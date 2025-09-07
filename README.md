# Pizza_sales_Project
## Pizza_sales SQL and Power BI Dashboard

This project is an end-to-end data analyst portfolio project focused on Pizza Sales Data for the year 2015, utilizing SQL Server and Power BI. It aims to build an interactive dashboard that provides comprehensive business insights.

## 📌  Project Overview

1) The main objective of the project  is to analyze pizza sales data from 2015 to build an interactive dashboard that provides comprehensive business insights.
2) The project covers a full spectrum of data analysis, from basic to advanced functionalities, including DAX functions, conditional filtering, conditional formatting, and action filters within Power BI.
3) A key aspect is validating Power BI results against SQL queries to ensure data accuracy and reliability.

 ### Data Import

• The raw data is provided in a CSV file named pizza_sales.csv containing sales information for the year 2015.

### 🔍 Data Exploration

• The pizza_sales dataset contains approximately 48,620 rows and 12 distinct fields (columns).

### Key columns and their significance include:

1) pizza_id: A unique identifier for each individual pizza sold (primary key).
2) order_id: Identifies specific customer orders; it can have duplicate entries if multiple pizzas were purchased in a single transaction within one order.
3) quantity: The number of pizzas ordered in a given row (typically small integer values).
4) date and time: The timestamp of when the order was placed.
5) unit_price and total_price: Pricing details for individual pizzas and the total for a specific pizza row.
6) size: Categorizes pizza sizes (e.g., Medium, Large, Small, X-Large, Double X-Large).
7) category: Classifies pizzas into types (e.g., Classic, Supreme, Chicken, Veg).
8) ingredients and name: Provides information about pizza toppings and specific pizza names.

### Date and Time Extractions/Transformations:
 
 1) Day Name: A Day Name column is extracted from order_date in Power Query to get names like Sunday, Monday, etc..
 2) Order Day (DAX): A new DAX column Order Day is created, extracting the first three uppercase letters of the Day Name (e.g., "FRI" for Friday).
 3) Day Number (Conditional Column in Power Query): A conditional column Day Number is created to assign numerical values (1-7) to each day of the week (Sunday=1, Monday=2, etc.). This is crucial for correct chronological sorting of daily trends in visuals
 4) Month Name (Power Query Editor): A Month Name column is extracted from order_date.
 5) Month Number (Power Query Editor): A Month Number column is extracted for sorting monthly trends.
 6) Order Month (DAX): Similar to Order Day, a DAX function extracts the first three uppercase letters of the Month Name (e.g., "JAN" for January)

###  📊 Business Insights

The project focuses on generating actionable business insights through several KPIs and interactive charts, with results validated against SQL queries.

• Key Performance Indicators (KPIs):

1) Total Revenue: The sum of total_price of all pizzas sold. (e.g., 817,860)
2) Average Order Value: Calculated as Total Revenue divided by Total Number of Orders. (e.g., 38.30).
3) Total Pizzas Sold: The sum of all quantity of pizzas sold. (e.g., 49,574).
4) Total Orders: The total number of distinct order_id values. (e.g., 21,350).
5) Average Pizzas Per Order: Total Pizzas Sold divided by Total Orders. (e.g., 2.32).
   
• Charts and Trends for Granular Insights:

1) Daily Trend for Total Orders (Column Chart): Shows daily order patterns, identifying busiest days (e.g., Friday, Saturday, and Thursday are often highest).
2) Monthly Trend for Orders (Line Chart): Illustrates monthly order trends, highlighting peak months (e.g., July, May, and January often show high orders).
3) Percentage of Sales by Pizza Category (Donut Chart): Visualizes the sales contribution and popularity of different pizza categories (e.g., Classic category contributes maximum sales).
4) Percentage of Sales by Pizza Size (Pie/Donut Chart): Shows customer preference for different pizza sizes (e.g., Large size pizzas contribute maximum sales).
5) Total Pizzas Sold by Pizza Category (Funnel Chart): Compares sales performance across categories, reinforcing insights about the highest selling categories (e.g., Classic category).
6) Top 5 Best Sellers (by Revenue, Quantity, Total Orders): Identifies the best-performing pizzas (e.g., Thai Chicken Pizza by revenue, Classic Deluxe Pizza by quantity and total orders) to guide marketing and discount strategies.
7) Bottom 5 Worst Sellers (by Revenue, Quantity, Total Orders): Identifies underperforming pizzas (e.g., Brie Care Pizza across all measures), informing decisions to stop production or remove items from the menu
