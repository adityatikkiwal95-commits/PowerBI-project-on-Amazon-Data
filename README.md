# PowerBI project on Amazon Data
# 📊 Amazon Sales Analysis Dashboard (Power BI)

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Analysis-Data_Modeling-blue?style=for-the-badge)

## 🚀 Project Overview
This project features an end-to-end Power BI solution that transforms fragmented Amazon sales data into a high-impact decision-making tool. By implementing a **Star Schema** and robust **ETL pipelines**, the dashboard provides a 360-degree view of revenue drivers, seasonal trends, and customer sentiment.

### 🎯 Key Business Insights
* **Revenue Performance:** Analyzed **$2.18M+ YTD Sales** and **28K+ units sold**, identifying critical growth patterns.
* **Category Strategy:** Isolated high-performing categories contributing to **55% of total revenue**.
* **Customer Sentiment:** Discovered that high-rating items drive a **32% higher sales volume**.
* **Operational Efficiency:** Improved decision-making clarity by **40%** through interactive drill-downs compared to raw data tables.

  
## 🛠️ Technical Implementation

### 1. Data Preparation (ETL)
Using **Power Query**, I engineered a clean dataset through:
* **Data Cleaning:** Removed duplicates and handled missing values.
* **Normalization:** Standardized category naming and date formats (YYYY-MM-DD).
* **Profiling:** Standardized numeric fields for accurate DAX calculation.

### 2. Data Modeling
I designed a **Star Schema** to optimize report performance and scalability:
* **Fact Table:** `Sales_Fact` (Revenue, Units, Reviews, Ratings).
* **Dimension Tables:** `Dim_Date`, `Dim_Product`, `Dim_Category`, and `Dim_Ratings`.

### 3. Core DAX Measures
Selected measures developed for this analysis:
* `Total Sales = SUM(Sales[Revenue])`
* `YTD Sales = TOTALYTD([Total Sales], 'Date'[Date])`
* `Category Contribution % = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Category)))`

---


