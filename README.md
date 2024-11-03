# Tokopedia Scraper

## Overview

Welcome to the **Tokopedia Scraper**! This project contains two scraping scripts to gather product information from Tokopedia using different approaches: **Selenium** and **Requests**. 

With this scraper, you can extract essential details about "flat shoes" available on Tokopedia, including the product name, store name, location, price, sold quantity, rating, and image URL.

## Features

- Scrape product details using **Selenium** for dynamic content.
- Scrape product details using **Requests** for static content.
- Save results in CSV format for easy access and analysis.

## Installation

### Prerequisites

Make sure you have the following installed on your machine:

- Python 3.1x.x
- Pip (Python package installer)
- Chrome WebDriver (for Selenium)

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/tokopedia-scraper.git
   cd tokopedia-scraper
   ```

2. Install the required packages:
   ```bash
   pip install requests beautifulsoup4 selenium pandas
   ```

3. Ensure that the Chrome WebDriver is compatible with your version of Google Chrome. Place the `chromedriver` file in the project directory.

## Usage

### Running the Scraper

To run the scrapers, simply execute the following commands in your terminal:

1. **Using Selenium:**
   ```bash
   python selenium_scraper.py
   ```

2. **Using Requests:**
   ```bash
   python requests_scraper.py
   ```

After running each script, the data will be saved in CSV files named:
- `result_scraping_tokped_with_selenium.csv`
- `result_scraping_tokped_with_requests.csv`

### Data Comparison

The data obtained from the **Selenium** scraper is generally more extensive because it utilizes a scrolling feature that loads more products as you scroll down the page, so it requires a relatively long execution time. In contrast, the **Requests** method captures only the products that are visible on the screen at the time of the request, leading to a more limited dataset and relatively fast execution time.

## Results

The following table shows the structure of the results generated by both scrapers:

| Name             | Store Name       | Location        | Price      | Sold   | Rating | Image URL                         |
|------------------|------------------|------------------|------------|--------|--------|-----------------------------------|
| Flat Shoes XYZ   | Shoe Store ABC   | Jakarta           | IDR 150,000| 25     | 4.5    | ![Image](http://example.com/image1.jpg) |
| Stylish Flats    | Trendy Shoes     | Bandung           | IDR 200,000| 10     | 4.0    | ![Image](http://example.com/image2.jpg) |

> Note: The above table is a sample representation of what you can expect in the CSV files.
---

Happy scraping!
