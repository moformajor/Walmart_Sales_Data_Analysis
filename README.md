# Walmart_Sales_Data_Analysis

## Overview 
In this project, we delve into Walmart sales data to gain insights into the performance of top branches and products, analyze sales trends across various product categories, and understand customer behavior. The overarching objective is to examine how sales strategies can be enhanced and optimized for better outcomes. The dataset utilized for this analysis originates from [the Kaggle Walmart Sales Forecasting ](https://www.kaggle.com/code/aslanahmedov/walmart-sales-forecasting)

## Aim of the Project
The primary objective of this project is to delve into Walmart's sales data, aiming to discern the various factors influencing the sales performance across its branches.

## Analysis List
1. Product Analysis
Analyze the data to gain insights into the diverse product lines, identify top-performing ones, and pinpoint areas for enhancement among the product lines.

2. Sales Analysis
This analysis seeks to uncover sales trends for products, offering valuable insights to gauge the efficacy of various sales strategies employed by the business and suggesting necessary modifications to enhance sales performance.

3. Customer Analysis
This analysis endeavors to unveil distinct customer segments, purchase patterns, and the profitability associated with each segment.

## Method Used
I. Data Cleaning: This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace, missing or NULL values.
- Build a database
- Create table and insert the data.
- Select columns with null values in them. There are no null values in our database as in creating the tables, we set NOT NULL for each field, hence null values are filtered out.

II. Feature Engineering: This will help use generate some new columns from existing ones.
- Add a new column named time_of_day to give insight of sales in the Morning, Afternoon and Evening. This will help answer the question on which part of the day most sales are made.
- Add a new column named day_name that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thur, Fri). This will help answer the question on which week of the day each branch is busiest.
- Add a new column named month_name that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit.
  
III. Exploratory Data Analysis (EDA): Exploratory data analysis is done to answer the listed questions and aims of this project.

## Some Business Questions Answered
1. Product
- How many unique product lines does the data have?
- What is the most common payment method?
- What is the most selling product line?
- What is the total revenue by month?
- What month had the largest COGS?
- What product line had the largest revenue?
- What is the city with the largest revenue?
- What product line had the largest VAT?
- Fetch each product line and add a column to those product line showing "Good", "Bad". Good if its greater than average sales
- Which branch sold more products than average product sold?
- What is the most common product line by gender?
- What is the average rating of each product line?

2. Sales
- Number of sales made in each time of the day per weekday
- Which of the customer types brings the most revenue?
- Which city has the largest tax percent/ VAT (Value Added Tax)?
- Which customer type pays the most in VAT?

3. Customer
- How many unique customer types does the data have?
- How many unique payment methods does the data have?
- What is the most common customer type?
- Which customer type buys the most?
- What is the gender of most of the customers?

# Queries sample
-- Most common payment method
SELECT payment_type, COUNT(payment_type) AS numbers
FROM sales
GROUP BY payment_type
ORDER BY numbers DESC;

-- What is the most selling product line?
SELECT product_line, COUNT(product_line) AS Qty
FROM sales
GROUP BY product_line
ORDER BY Qty DESC;

For the rest of the full queries, check the [Data Exploration of walmart sales.sql](https://github.com/moformajor/Walmart_Sales_Data_Analysis/blob/main/Data%20Exploration%20of%20walmart%20sales.sql) file
