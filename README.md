Project Overview:
This project is designed to analyze and visualize customer spending behavior using transaction data, including city, customer age, product type, spend amount, repayment amount, and transaction dates. It uncovers insights into customer spending patterns, repayment trends, and product preferences across various cities and demographics.

Objective:
The primary objective of this analysis is to gain actionable insights into customer behavior that can assist financial institutions in improving their offerings and targeting their marketing efforts effectively.

Key Features:
City-wise Spend Analysis: Identifies which city has the highest total spend.
Age Group Spend Analysis: Determines which age group contributes the most to the total spend.
Top Repayment Customers: Lists the top 10 customers based on repayment amounts.
Yearly Spend on Products: Analyzes spending on various product types year-by-year, broken down by city.
Data Visualizations: Provides various visual representations of spend data, including city-wise and product-wise trends.
User-Defined Analysis: A function is provided for the user to dynamically analyze top 10 customers for a specified product and time period (yearly or monthly).
Steps Taken in the Project:
1. Data Preprocessing:
Loaded transaction data (spend, repayment, and customer acquisition data) and merged it into a unified table.
Cleaned the data by handling edge cases:
Replaced ages less than 18 with the mean age.
Ensured spend amounts did not exceed a customer's per-transaction limit.
Adjusted repayment amounts that exceeded the customer's limit.
2. Data Exploration and Summarization:
Calculated the number of distinct customers.
Identified distinct product categories.
Calculated average monthly spend and repayment amounts.
Identified the bank’s profit by calculating interest on monthly profit (only positive profits).
Analyzed the top 5 most purchased product types.
Found the city with the highest spend and the age group spending the most money.
Listed the top 10 customers based on repayment amount.
3. City-wise & Product-wise Analysis:
Analyzed yearly spend on products across different cities.
Generated various plots to visualize the data, including:
A heatmap showing yearly spend on each product across cities.
Monthly comparison of total spends by city.
Yearly spend on air tickets.
Comparison of monthly spend for each product to detect seasonality.
4. User-Defined Function for Customer Analysis:
Created a Python function (top_customers_analysis) to allow dynamic analysis of the top 10 customers based on repayment amount, filtered by product and time period (monthly or yearly).
Key Python Functions and Libraries Used:
Libraries:

pandas: For data manipulation and analysis.
matplotlib and seaborn: For creating visualizations.
Functions:

top_customers_analysis: Custom function to filter and analyze the top 10 customers based on product type and time period.
Data Cleaning:

Handled missing or erroneous data such as adjusting age, spend amount, and repayment amount.
How This Analysis Helps:
Targeted Marketing: By understanding which products are most popular in specific cities, banks can target their marketing efforts more effectively.
Customer Behavior Insights: Identifying top repayment customers and spending patterns based on age or city allows the bank to personalize offers.
Profit Maximization: The profit analysis helps the bank optimize its offerings and loan repayment structures to maximize interest earnings.
Seasonal Insights: By analyzing product-wise spending trends, banks can adjust their offerings and promotions based on seasonality patterns.
How to Run the Code:
Clone this repository to your local machine.
Install necessary libraries using pip install pandas numpy matplotlib seaborn.
Place the data files (spend.csv, Repayment.csv, Customer Acqusition.csv) in the working directory.
Run the Jupyter notebook or Python script to execute the analysis.
Visualizations will be displayed for key trends, and outputs such as the top 10 customers will be printed.
Sample Function Usage:
To find the top 10 customers for a specific product type and time period, use the following function:

python
Copy
Edit
top_customers = top_customers_analysis(final_tab, 'Gold', 'yearly')

for city, df_top_customers in top_customers.items():
    print(f"Top 10 customers in {city} for Gold (yearly):")
    print(df_top_customers[['Customer', 'Period', 'Repayment_Amount']])
    print()
Future Improvements:
Modeling: Integrating predictive analytics to forecast customer behavior such as repayment amounts or spend patterns.
More Visualizations: Additional types of graphs could be used, such as pie charts for product distribution or scatter plots for spend vs. repayment amounts.
Real-time Data Analysis: The project can be expanded to work with live transaction data for real-time analytics.
