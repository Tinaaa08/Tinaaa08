# Project Summary – Falcon 9 Booster Data Scraping

## Selected Scraper: Beautiful Soup

For this project, I decided to use **Beautiful Soup** as my main scraping tool. After trying out both Beautiful Soup and Scrapy, I found that Beautiful Soup was much easier to understand and use. It has great documentation and worked well with other Python libraries I was already familiar with, like requests and pandas. It also made it pretty simple to pull the data from the Wikipedia tables in the website. 

The overall process of getting the Beautiful Soup scraper to work took **about 8 hours over the period of 2 days**. I spent time figuring out how the Wikepedia tables were structured.  One of the trickier parts was keeping track of the booster ID and block type since some boosters spanned multiple rows, so that made it harder to extract the data. I specifically had trouble with the turnaround time. After many tries it finally worked, but at first the turnaround column was empty. 

Working with Beautiful Soup gave me a much better understanding of how to navigate and extract data from HTML, and I feel more confident using it for future web scraping projects.

## ScrapeGraphAI Prompts and Strategy

Alongside traditional scraping, I used **ScrapeGraphAI** to get the same data using prompts. Below is a summary of the prompts I used to extract the data:

- **Only Falcon 9 Launches:**  
  _"Extract only Falcon 9 launches (flight numbers starting with F9-) from the Wikipedia page and return all relevant details in a structured table."_

- **Only Falcon Heavy Launches:**  
  _"Extract only Falcon Heavy launches from the Wikipedia page List of Falcon 9 first-stage boosters, where the flight number starts with FH-, and return all relevant launch details in a structured table."_

- **Three Engines in Each Falcon Heavy Launch:**  
  _"Extract the three boosters used in each Falcon Heavy launch from the Wikipedia page List of Falcon 9 first-stage boosters, and return them grouped by their shared Falcon Heavy flight number in a structured table."_

- **Block 1 or 1.1 Launch**
  _"Extract only the launches using Block 1 or Block 1.1 engines from the Wikipedia page List of Falcon 9 first-stage boosters, and return the relevant launch details in a structured table."

- **Block 4 Launch**
  _"Extract only the launches using Block 4 engines from the Wikipedia page List of Falcon 9 first-stage boosters, and return the relevant launch details in a structured table."

- **Block 5 Launch**
  _"Extract only the launches that used Block 5 engines from the Wikipedia page List of Falcon 9 first-stage boosters, and return the relevant launch details in a structured table."

- **Longest Turnaround Times:**  
  _"From the Wikipedia page List of Falcon 9 first-stage boosters, extract all turnaround times for Block 4 and Block 5 boosters, and return only the single highest turnaround time in days as a number."_

- **Fastest Turnaround Times:**
  _"From the Wikipedia page List of Falcon 9 first-stage boosters, extract all turnaround times for Block 4 and Block 5 boosters , and return the fastest turnaround time in days as a single number."_
  
- **Most Launches by a Booster:**  
  _"From the Wikipedia page List of Falcon 9 first-stage boosters, extract the total number of Launches for each Block 4 and Block 5 booster, and return only the highest number of Launches as a whole number."_

### Prompt Strategy

When I was writing each prompt, I tried to keep things clear and specific. I used words like "only" or "where the flight number starts with..." to make sure the output focused on exactly what I needed. I also made sure to ask for things like a "structured table" or "a single number" so the format stayed consistent. This step-by-step approach made it easier for ScrapeGraphAI to understand what I wanted and avoid pulling in the wrong data. 

## Development Tools Used

I primarily used:
- **VSCode** for testing my Python scripts.
- **Jupyter Notebook** for writing my code and testing it before I transferred it to Visual Studio Code. 
- **ScrapeGraphAI** for webscraping using AI.
- **Spyder** for running the ScrapeGraphAI code.

These tools made it easier for me to write, test, and fix my code, and also check that the results were accurate using both regular scraping and AI-based methods.

## Development Plan and Challenges

My plan was to start by using Beautiful Soup to manually scrape and process the data. After that, I created separate output files for each part of the assignment. I also worked on the AI prompts by testing them out one at a time to see what worked and what didn’t, and then adjusted the prompts based on the results.

Some **challenges** I ran into were:
- Figuring out how to work with Wikipedia tables that had boosters spread across multiple rows 
- Making sure the turnaround times matched the right booster
- Running out of ScrapeGraphAI credits quickly, which meant I had to find and use multiple emails to create new accounts just to finish all the prompts
- Learning how to use ScrapeGraphAI
- Understanding exactly what the question was asking so I knew how to proceed

Overall, using both Beautiful Soup and ScrapeGraphAI helped me double-check my results in two different ways, which made the data more accurate and gave me more confidence in what I was getting. This project really helped me understand how web scraping works. I learned how to read and work with HTML, write clear prompts, and handle messy data. I now feel a lot more comfortable with web scraping and how to pull out the exact information I need for future projects.
