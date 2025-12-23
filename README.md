# Global Bank Capitalization ETL Pipeline

## Project Overview
This project is an automated **ETL (Extract, Transform, Load)** pipeline designed to identify the top 10 largest banks in the world by market capitalization.

The pipeline extracts raw data from Wikipedia, transforms the financial data into multiple currencies (GBP, EUR, INR) using exchange rates, and loads the processed data into both a CSV file and a local SQLite database for querying.

## Key Features
* **Web Scraping:** Automated extraction of HTML tables using `BeautifulSoup`.
* **Data Transformation:** Conversion of market cap data based on exchange rates:
    * 1 USD = 0.8 GBP
    * 1 USD = 0.93 EUR
    * 1 USD = 82.95 INR
* **Database Integration:** Seamless loading of processed data into a SQLite database.
* **Logging:** Implementation of a `log_progress()` function to track pipeline execution timestamps.

## Technologies Used
* **Language:** Python 3.x
* **Libraries:** `Pandas`, `NumPy`, `BeautifulSoup` (bs4), `Requests`, `SQLite3`, `Datetime`

## Project Workflow
1.  **Extract:** Scrape raw data from the provided URL.
2.  **Transform:** Clean data, convert data types, and apply currency exchange calculations.
3.  **Load:** Save the final dataset as `Largest_banks_data.csv` and inject it into the `Banks.db` database.
4.  **Query:** Execute SQL queries to verify data integrity and analyze results.
