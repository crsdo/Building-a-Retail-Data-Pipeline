# Walmart E-Commerce Sales Analysis

## Overview

This project focuses on analyzing the impact of public holidays on Walmart's sales, particularly within their e-commerce sector. By the end of 2022, Walmart's e-commerce sales reached an impressive $80 billion, accounting for 13% of total sales. Understanding the sales trends around key holidays like the Super Bowl, Labour Day, Thanksgiving, and Christmas will provide valuable insights for future strategies.

## Project Structure

The project involves creating a data pipeline to analyze supply and demand related to holidays. You will work with two primary data sources:

1. **grocery_sales** (PostgreSQL database)
   - **index**: Unique ID of the row
   - **Store_ID**: Store number
   - **Date**: Week of sales
   - **Weekly_Sales**: Sales for the given store

2. **extra_data.parquet** (Complementary data)
   - **IsHoliday**: Indicates if the week contains a public holiday (1 if yes, 0 if no)
   - **Temperature**: Temperature on the day of sale
   - **Fuel_Price**: Cost of fuel in the region
   - **CPI**: Consumer price index
   - **Unemployment**: Unemployment rate
   - **MarkDown1, MarkDown2, MarkDown3, MarkDown4**: Promotional markdowns
   - **Dept**: Department number in each store
   - **Size**: Size of the store
   - **Type**: Type of the store (based on size)

## Objectives

1. **Data Merging**: Combine the `grocery_sales` and `extra_data` files into a single DataFrame.
2. **Data Transformation**: Clean and manipulate the merged data to create a new DataFrame (`clean_data`) with the following columns:
   - **Store_ID**
   - **Month**
   - **Dept**
   - **IsHoliday**
   - **Weekly_Sales**
   - **CPI**
   - **Unemployment**

3. **Aggregation**: Perform a monthly sales analysis and store the results in a variable (`agg_data`) that contains:
   - **Month**
   - **Weekly_Sales**

4. **Export**: Save the `clean_data` and `agg_data` DataFrames as CSV files for further analysis.

## Requirements

- Python 3.x
- Pandas
- PostgreSQL (for accessing the grocery sales data)


