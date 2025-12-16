📊 Retail Sales Analytics with Databricks & PySpark

An end-to-end big data analytics project demonstrating scalable data processing and business intelligence using Databricks Community Edition and Apache Spark (PySpark). This project ingests a real-world retail dataset from Kaggle, performs comprehensive cleaning and transformation, and delivers actionable business insights through advanced analytics and visualizations.

🔗 Live Databricks Notebook
[Open the Interactive Notebook Here](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3675438403174862/3900883391960238/2977761025472207/latest.html)
Note: This public link is valid for approximately 6 months from its creation.
________________________________________________
📋 Project Overview
This project implements a full data analytics pipeline:

Data Ingestion: Automated download of a Kaggle dataset directly into Databricks.

Data Processing: Cleaning, transformation, and feature engineering using PySpark.

Advanced Analytics: Customer segmentation, trend analysis, and profitability studies.

Visualization & Reporting: Generation of key business metrics and professional charts.
________________________________________________
🛠️ Technology Stack
Category	Tools & Libraries
Cloud Platform	Databricks Community Edition
Processing Engine	Apache Spark 3.x (PySpark API)
Core Libraries	pyspark.sql, pyspark.sql.functions
Data Visualization	Matplotlib, Seaborn
Data Management	Pandas (for charting), KaggleHub API
Storage Format	Parquet (for optimized results)
________________________________________________
📁 Project Folder Structure (in Databricks DBFS)

/FileStore/

├── kaggle/                          # Raw dataset downloaded from Kaggle

│   └── superstore/train.csv

├── parquet/                         # Optimized analysis outputs

│   ├── rfm_analysis.parquet

│   ├── quarterly_sales.parquet

│   └── customer_lifetime_value.parquet

├── results/                         # Final reports and results

│   └── retail_analytics_report.md

├── charts/                          # Generated visualization PNG files

│   ├── quarterly_sales_trend.png

│   ├── category_performance.png

│   ├── rfm_segmentation.png

│   ├── monthly_trend_line.png

│   ├── top_customers.png

│   └── shipping_performance.png

└── portfolio/                       # Assets for GitHub portfolio

    └── project_summary.md
________________________________________________

📂 Dataset Information
Source: Kaggle: Sales Forecasting Dataset by rohitsahoo

File Used: train.csv

Records: 9,800 sales transactions

Time Period: January 2015 to December 2018 (4 years)

Key Columns: Order ID, Date, Customer, Product Category, Sales, Region, Ship Mode.
________________________________________________

📈 Key Business Metrics Calculated
The analysis computed the following core metrics:

Total Revenue: Sum of all Sales.

Average Order Value (AOV): Mean of Sales.

Customer Base: Count of distinct Customer ID.

Order Volume: Count of distinct Order ID.

Shipping Efficiency: Average shipping_days (derived from Ship Date - Order Date).

Year-over-Year (YoY) Growth: Percentage change in quarterly sales.
________________________________________________

⚙️ PySpark & Spark SQL Functions Used
The notebook extensively uses PySpark's DataFrame API and functions for transformation and aggregation:

🔧 Data Transformation & Cleaning

to_date(): Convert string columns to DateType.

withColumn() / withColumnRenamed(): Create new or rename columns.

cast(): Change column data types (e.g., String to Double).

when() / otherwise(): Implement conditional logic (similar to SQL CASE WHEN).

regexp_replace(): Clean string values (e.g., remove currency symbols from sales).

year(), month(), quarter(): Extract date parts for trend analysis.

datediff(): Calculate the difference in days between two dates (for shipping time).
________________________________________________

📊 Aggregation & Analysis
groupBy(): Group data for aggregate calculations.

agg(): Perform multiple aggregations (sum, count, average).

sum() / avg() / count() / countDistinct(): Basic aggregate functions.

min() / max(): Find minimum and maximum values.

orderBy(): Sort results.

describe(): Generate summary statistics.

________________________________________________
🎯 Advanced Analytics (Window Functions & SQL)
Window() + orderBy(): Define window specifications.

ntile(): Assign percentile ranks (used for RFM scoring).

lag(): Access data from a previous row in the same result set (used for YoY growth calculation).

createOrReplaceTempView(): Register a DataFrame as a temporary SQL view.

Spark SQL Queries: Direct SQL syntax (e.g., %sql SELECT ...) was used for complex joins and analysis.
________________________________________________

📊 Generated Visualizations (PNG Files)
The project created six key charts, saved as high-resolution PNG files:
1. Quarterly Sales Performance (2015-2018)
https://charts/quarterly_sales_trend.png
Bar chart showing sales performance across all quarters (2015-2018).

2. Product Category Distribution
https://charts/category_performance.png
Pie chart displaying revenue distribution across Furniture, Office Supplies, and Technology.

3. Customer RFM Segmentation
https://charts/rfm_segmentation.png
Bar chart visualizing the 8 customer segments (Champions, Loyal, At Risk, etc.) from the RFM analysis.

4. Monthly Sales Trend
https://charts/monthly_trend_line.png
Line chart with a trend line illustrating sales over the last 24 months.

5. Top Customers by Lifetime Value
https://charts/top_customers.png
Horizontal bar chart ranking the top 10 customers by Lifetime Value (LTV).

 6. Shipping Mode Performance
https://charts/shipping_performance.png
Dual chart comparing shipping mode volume (pie) and average speed (bar).
________________________________________________

📝 Key Insights Summary
Sales Trend: Strong growth observed, with Q4 2018 being the peak sales quarter.

Top Category: Technology generated the highest revenue, with Phones as the leading sub-category.

Customer Segments: RFM analysis identified 195 "Champion" customers who are the most valuable.

Shipping: "Standard Class" is the most common but slowest mode; "Same Day" shipping is most efficient in the West region.

Geography: California (West region) is the top-performing state by sales volume.

________________________________________________

📊 FINAL PROJECT SUMMARY & KEY METRICS
============================================================
RETAIL SALES ANALYTICS - SUPERSTORE DATASET
============================================================

📈 KEY PERFORMANCE METRICS:
----------------------------------------
💰 Total Revenue:          $2,237,133.16
📦 Total Orders:           4,922
👥 Unique Customers:       793
📊 Average Order Value:    $235.29
📅 Analysis Period:        2015-01-03 to 2018-12-30
📦 Products Analyzed:      1,861
🚚 Avg Shipping Days:      3.96 days

🔍 TOP BUSINESS FINDINGS:
----------------------------------------
1. 📈 Q4 2018 was the best quarter with $274,516 in sales
2. 🏆 Technology category generated highest revenue
3. 👑 195 'Champion' customers drive 40% of total revenue
4. 🚀 Sales grew 18.86% YoY in latest quarter
5. 📦 Standard Class shipping is most used but slowest (5+ days)
6. 🤝 Office Supplies + Technology is most common product bundle
7. 🏆 Top customer 'Sean Miller' spent $25,043 across 5 orders
8. 🌍 West region has fastest 'Same Day' shipping efficiency

________________________________________________
✨ Skills Demonstrated
This project showcases practical skills in:

Building production-style data pipelines on Databricks.

Performing large-scale data wrangling with PySpark DataFrames.

Implementing advanced analytics (RFM, CLV, Time Series).

Translating data insights into clear business recommendations.

Creating automated reports and professional visualizations.

This project was developed as a portfolio piece to demonstrate end-to-end competency in Big Data analytics.
Analyst: Buvi | Tools: Databricks, PySpark, Python

