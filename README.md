# README

## Overview
This script scrapes data from the VCS Data website, specifically targeting the "Hospitals/Healthcare" industry in India. The script extracts company names, addresses, and industry types, then saves the data into a CSV file.

## Requirements
- Python 3.10
- Required libraries: `requests`, `bs4` (BeautifulSoup), `pandas`, `numpy`

You can install the required libraries using pip:
```bash
pip install requests beautifulsoup4 pandas numpy
```

## Script Explanation
The script performs the following steps:
1. Initializes empty lists to store company names, addresses, and industry types.
2. Iterates over the pages of the target website (from page 1 to 466).
3. Sends an HTTP GET request to fetch the page content.
4. Parses the HTML content using BeautifulSoup.
5. Extracts relevant information from the parsed HTML and appends it to the respective lists.
6. Combines the data into a NumPy array, transposes it, and converts it into a Pandas DataFrame.
7. Saves the DataFrame as a CSV file named `companyDetails.csv`.

## Usage
1. **Run the Script:**
   - Ensure you have Python installed on your system.
   - Install the required libraries as mentioned above.
   - Execute the script using the command:
     ```bash
     python script_name.py
     ```
   - Replace `script_name.py` with the actual name of the script file.

2. **Output:**
   - The script will print a message indicating the completion of each page.
   - After processing all pages, the data will be saved in a CSV file named `companyDetails.csv` in the current directory.

## Script Details

### Variables
- `company_names`: List to store the names of companies.
- `company_address`: List to store the addresses of companies.
- `industry_type`: List to store the industry types.

### Functions and Methods
- `requests.get()`: Sends an HTTP GET request to the target URL.
- `BeautifulSoup()`: Parses HTML content.
- `findAll()`: Finds all matching elements in the parsed HTML.
- `find()`: Finds the first matching element in the parsed HTML.
- `append()`: Appends an element to a list.
- `np.array()`: Creates a NumPy array.
- `pd.DataFrame()`: Creates a Pandas DataFrame.
- `to_csv()`: Saves the DataFrame as a CSV file.

### URL and Headers
- `URL`: Formatted URL to access different pages of the website.
- `headers`: HTTP headers to mimic a browser request, which helps in avoiding blocking by the website.

## Notes
- Ensure you have a stable internet connection while running the script, as it makes multiple HTTP requests.
- The script might take some time to complete as it processes 466 pages.
- The CSV file will be created in the directory where the script is executed.

This README provides a comprehensive guide on how to use the script to scrape hospital and healthcare company data from the VCS Data website and save it to a CSV file.
