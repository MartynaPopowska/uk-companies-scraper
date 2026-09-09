UK Companies House Web Scraper
Martyna Popowska

PROJECT DESCRIPTION:
This project automates the extraction and cleaning of business data from the UK Companies House registry. Due to the server's anti-bot protections and dynamic content, I implemented a hybrid extraction pipeline using multiple Python tools to ensure reliable data harvesting while adhering to ethical scraping practices.

TECHNOLOGIES USED:
1. Scrapy - Deployed to navigate the initial search index and harvest company profile URLs.
2. Requests & BeautifulSoup - Used together for rapid static HTML parsing. I applied custom headers in Requests to bypass basic WAF blocks, and BeautifulSoup to precisely extract core text data (applying string manipulation like removing the "overview" suffix to ensure high data quality).
3. Selenium - Used to simulate a real web browser environment to perform dynamic interactions, specifically simulating a click on the 'People' tab. Implemented with webdriver-manager for execution stability.
4. Pandas - Utilized to structure the scraped data into a dataframe and export it to a clean CSV file.
5. Regular Expressions (re module) - Applied re.findall() to extract exact alphanumeric UK postcodes from unstructured address strings, and re.match() to validate the official format of company numbers.

HOW TO RUN THE PROJECT:
1. Install the required libraries by running: pip install -r requirements.txt
2. Open the Jupyter Notebook file (uk_companies_house_data_extraction.ipynb) and run the cells sequentially from top to bottom. (Note: The Scrapy script 'ch_scraper.py' from the 'scripts' folder will be automatically executed in the background by the notebook).
3. The generated .json (extracted links) and .csv (final cleaned dataframe) files will be automatically saved in the 'outputs' directory.
