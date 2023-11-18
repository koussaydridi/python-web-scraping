# Web Scraping and Data Analysis

## Overview
This Python script demonstrates web scraping using BeautifulSoup to extract information from a Wikipedia page. The data is then processed and stored in a Pandas DataFrame before being exported to an Excel file.

## Instructions
1. Install the required libraries by running:
    ```bash
    pip install beautifulsoup4 requests pandas
    ```

2. Run the script:
    ```bash
    python script_name.ipynb
    ```

## Code Explanation

### 1. Importing Libraries
- `from bs4 import BeautifulSoup`: Importing BeautifulSoup for HTML parsing.
- `import requests`: Importing the requests library for making HTTP requests.
- `import pandas as pd`: Importing Pandas for data manipulation.

### 2. Retrieving Web Page
- `url = 'https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue'`: Setting the URL to scrape.
- `page = requests.get(url)`: Sending a GET request to the URL.

### 3. Parsing HTML Content
- `soup = BeautifulSoup(page.text, 'html')`: Creating a BeautifulSoup object to parse HTML content.

### 4. Extracting Table Data
- `table = soup.find_all('table')[1]`: Extracting the second table from the HTML.
- `word_title = table.find_all('th')`: Extracting table headers.

### 5. Creating DataFrame
- `df = pd.DataFrame(columns=word_table_text)`: Creating an empty DataFrame with column headers.

### 6. Populating DataFrame
- Looping through table rows, extracting data, and populating the DataFrame.

### 7. Exporting Data
- `df.to_excel(r'C:\Users\HP\Desktop\Python\companies.xlsx', index=False)`: Exporting DataFrame to an Excel file.

## Note
- Make sure to customize file paths and names according to your preferences.
- Ensure proper installation of required libraries before running the script.

# Data Visualization with Matplotlib

## Overview
This Python script demonstrates data visualization using Matplotlib. It reads data from an Excel file, creates a histogram, and visualizes the distribution of a specific column.

## Instructions
1. Install the required libraries by running:
    ```bash
    pip install matplotlib pandas
    ```

2. Update the file path:
   - Replace `"C:\Users\HP\Desktop\Python\companies.xlsx"` with the path to your Excel file.

3. Run the script:
    ```bash
    python data_visualization.py
    ```

