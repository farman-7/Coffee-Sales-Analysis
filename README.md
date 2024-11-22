Coffee Sales Analysis Project 🚀


Overview
Coffee Sales Analysis leverages SQL and Power BI to explore sales trends, customer behavior, and product performance. This interactive project provides valuable insights into sales patterns, enabling data-driven decision-making.

👉 Live Dashboard Demo: View Dashboard
👉 Project Walkthrough Video: Watch on YouTube

📌 Table of Contents
Problem Statement
Steps in SQL
SQL Functionalities Used
Key Performance Indicators (KPIs)
Charts and Visualizations
Tools and Technologies
Project Highlights
Problem Statement
Businesses often struggle to identify patterns and trends in their sales data. This project aims to answer the following:

Which months had the highest and lowest sales?
Do sales differ between weekdays and weekends?
Which store locations and products are top performers?
How can visual analytics provide actionable insights?
Steps in SQL
Data Walkthrough
Data Preparation: Organize raw data files.
Database Creation: Create a structured database.
Data Cleaning: Fix errors, handle null values, and adjust data types.
SQL Queries:
Analyzed sales, orders, and quantities month-on-month.
Used window functions for comparative metrics.
Aggregated data to support visualizations.
👉 Example SQL Query:

sql
Copy code
SELECT  
    DATE_FORMAT(order_date, '%Y-%m') AS Month,  
    SUM(sales) AS Total_Sales,  
    LAG(SUM(sales)) OVER (ORDER BY DATE_FORMAT(order_date, '%Y-%m')) AS Previous_Month_Sales,  
    (SUM(sales) - LAG(SUM(sales)) OVER (ORDER BY DATE_FORMAT(order_date, '%Y-%m'))) AS Sales_Difference  
FROM sales_data  
GROUP BY Month;  
SQL Functionalities Used
Here are the key SQL techniques applied:

Category	Functions
Date Functions	STR_TO_DATE, DAY, MONTH, HOUR, DAYOFWEEK
Aggregations	SUM, COUNT, AVG, MAX, MIN
Conditionals	CASE, WHERE, GROUP BY, ORDER BY
Table Modifications	ALTER TABLE, UPDATE TABLE, CHANGE COLUMN
Window Functions	LAG, ROW_NUMBER
Joins & Queries	JOINS, SUBQUERIES, LIMIT, ALIAS
Key Performance Indicators (KPIs)
Here are the actionable insights generated:

Total Sales Analysis: Monthly sales trends and MoM growth rates.
Total Orders Analysis: Order volumes and differences across months.
Quantity Sold Analysis: Quantity trends and highlights.
👉 Insight Example:

"Sales peaked in December, with a 15% increase from November. Weekday sales outperformed weekends by 20%."

Charts and Visualizations
Sample Dashboards
Calendar Heat Map: Visualizes daily sales with darker shades for higher values.
Sales by Weekday vs. Weekend: Highlights performance variations.
Store Location Analysis: MoM comparisons for each location.
Daily Sales with Average Line: Identifies exceptional sales days.
Top Products by Sales: Displays the top 10 products dynamically.
👉 Screenshot Example:


Tools and Technologies
SQL: Data cleaning, processing, and analysis.
Power BI: Interactive dashboards and visualizations.
Excel: Initial data preparation and validation.
Project Highlights
Dynamic Visualizations: Dashboards adapt based on slicer inputs.
Optimized Queries: Used advanced SQL techniques for faster performance.
Business Value: Insights are directly actionable for sales strategy optimization.
📧 Contact Me

Email: farman@example.com
LinkedIn: Farman's Profile
Portfolio: Visit My Portfolio
