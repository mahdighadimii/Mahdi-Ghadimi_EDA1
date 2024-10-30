# Mahdi Ghadimi - Performing exploratory data analysis on retail data with Python


## Overview
In this project, you will step into the shoes of an entry-level data 
analyst at an online retail company, helping interpret real-world data 
to help make a key business decision.

## Case Study
In this project, you will be working with transactional data from an 
online retail store. The dataset contains information about customer 
purchases, including product details, quantities, prices, and 
timestamps. Your task is to explore and analyze this dataset to gain 
insights into the store's sales trends, customer behavior, and popular 
products.

By conducting exploratory data analysis, you will identify patterns, 
outliers, and correlations in the data, allowing you to make data-driven 
decisions and recommendations to optimize the store's operations and 
improve customer satisfaction. Through visualizations and statistical 
analysis, you will uncover key trends, such as the busiest sales months, 
best-selling products, and the store's most valuable customers. 
Ultimately, this project aims to provide actionable insights that can 
drive strategic business decisions and enhance the store's overall 
performance in the competitive online retail market.

## Prerequisites
Before starting this project, you should have some basic knowledge of 
Python programming and Pandas. In addition, you may want to use the 
following packages in your Python environment:

- pandas
- numpy
- seaborn
- matplotlib

These packages should already be installed in Coursera's Jupyter 
Notebook environment; however, if you'd like to install additional 
packages that are not included in this environment or are working off 
platform, you can install additional packages using `!pip install packagename` within a notebook cell such as:
```python
!pip install pandas
!pip install matplotlib
```

## Project Objectives
- Describe data to answer key questions to uncover insights
- Gain valuable insights that will help improve online retail performance
- Provide analytic insights and data-driven recommendations

## Dataset
The dataset you will be working with is the "Online Retail" dataset. 
It contains transactional data of an online retail store from 2010 to 
2011. The dataset is available as a `.xlsx` file named `Online Retail.xlsx`. 
This data file is already included in the Coursera Jupyter Notebook 
environment; however, if you are working off-platform, it can also be 
downloaded [here](#).

The dataset contains the following columns:
- **InvoiceNo**: Invoice number of the transaction
- **StockCode**: Unique code of the product
- **Description**: Description of the product
- **Quantity**: Quantity of the product in the transaction
- **InvoiceDate**: Date and time of the transaction
- **UnitPrice**: Unit price of the product
- **CustomerID**: Unique identifier of the customer
- **Country**: Country where the transaction occurred

## Tasks
You may explore this dataset in any way you would like. However, if you'd like some help getting started, here are a few ideas:
1. Load the dataset into a Pandas DataFrame and display the first few rows to get an overview of the data.
2. Perform data cleaning by handling missing values, if any, and removing any redundant or unnecessary columns.
3. Explore the basic statistics of the dataset, including measures of central tendency and dispersion.
4. Perform data visualization to gain insights into the dataset. Generate appropriate plots, such as histograms, scatter plots, or bar plots, to visualize different aspects of the data.
5. Analyze the sales trends over time. Identify the busiest months and days of the week in terms of sales.
6. Explore the top-selling products and countries based on the quantity sold.
7. Identify any outliers or anomalies in the dataset and discuss their potential impact on the analysis.
8. Draw conclusions and summarize your findings from the exploratory data analysis.


# Results:

## Summary
This project performs an Exploratory Data Analysis (EDA) on an online retail dataset, using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn. 
Through EDA, we identified valuable insights, such as sales trends, top-performing products, and customer behavior patterns. The project involved data cleaning, 
handling missing values, identifying outliers, and visualizing sales trends. These insights can be used to improve business operations and customer satisfaction. 
For example, the identification of top-selling products and peak sales periods enables better inventory planning and marketing strategies.

## Overview
In this analysis, we worked with real-world retail transaction data from an online store. The data included key columns like product descriptions, quantities, sales prices, 
and transaction timestamps. Our objectives were to analyze trends, find best-selling products, and explore customer behavior over time. Insights derived from this analysis 
can help the business optimize inventory, adjust marketing strategies, and understand the most valuable customers and peak sales periods.

## Project Objectives
- **Data Exploration**: Analyze patterns, trends, and relationships in the data.
- **Sales Optimization**: Identify peak sales months, best-selling products, and customer preferences to enhance inventory management and marketing efforts.
- **Actionable Recommendations**: Provide data-driven insights to guide business strategies.

## Data Cleaning Process
The data contained 541,909 records, and our initial steps involved:
- **Dropping redundant columns**: We removed InvoiceNo, StockCode, and CustomerID as they were not relevant for our analysis.
- **Handling duplicates**: Found and removed 6,183 duplicate rows.
- **Managing missing values**: Identified 1,370 missing product descriptions and dropped these rows to ensure data quality.
- **Ensuring correct data types**: Converted InvoiceDate to datetime format to enable time-based analysis.

## Analysis and Key Findings
### Sales Trends Over Time
- **Monthly Sales**:  
  Sales peaked in November and December, likely driven by holiday shopping.  
  Sales were lower during the summer months, indicating seasonal demand.  
  - *Plot*: A bar chart showed November as the busiest month.

- **Day-of-Week Sales Pattern**:  
  Most sales transactions occurred on Wednesdays and Thursdays.  
  The fewest transactions were recorded on Sundays.

### Top-Selling Products
- Products like “WHITE HANGING HEART T-LIGHT HOLDER” and “PACK OF 20 SPACEBOY NAPKINS” were among the top-selling items.  
  This suggests demand for home decor and novelty items.  
  - *Plot*: A bar plot visualized the top 70 products based on the total quantity sold.

### Outlier Analysis
- We detected several outliers in Quantity and UnitPrice.  
  Some transactions recorded negative or unusually high quantities, possibly representing order cancellations or data entry errors.  
  The IQR (Interquartile Range) technique helped us filter out these outliers, reducing the dataset to 404,023 records.

### Correlation Analysis
- A heatmap revealed weak correlations between numerical variables.  
  Quantity sold and unit price had almost no correlation, suggesting pricing does not heavily impact product demand.

## Data Visualization Highlights
- **Bar Charts**: Illustrated the busiest sales months and most popular products.
- **Boxplots**: Helped detect outliers in quantities and unit prices.
- **Scatter Plots**: Showed relationships between variables like Quantity vs. Month.
- **Heatmap**: Provided a correlation matrix of numerical columns, offering insight into how features relate to each other.

## Recommendations and Business Impact
### Inventory Planning
- Ensure higher stock levels for top-selling products like T-light holders during November and December.
- Focus on seasonal campaigns during peak months to maximize revenue.

### Sales Promotion on Weekdays
- Encourage more weekday sales (especially Wednesdays) by offering discounts or free shipping, as these days show the highest activity.

### Improve Data Quality
- Address negative and high-quantity orders by refining data entry processes or automating cancellation logging.

### Product Strategy
- Continue offering home decor products as they perform well.  
  Consider bundling or creating similar novelty products to increase sales further.
