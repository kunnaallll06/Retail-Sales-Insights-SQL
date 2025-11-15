# 📊 Retail Sales Insights using SQL  
### End-to-End Data Analysis Project (Customer, Product & Sales Insights)

This project focuses on analyzing **Retail Sales Performance**, **Customer Segmentation**, and **Product-Level Insights** using **SQL Server**.  
It includes complete scripts, datasets, documentation, and analytical reports built using advanced SQL.

---

## 🔍 Project Overview
The goal of this project is to perform a full analytics workflow:

- Data Cleaning  
- Data Aggregation  
- Customer & Product Segmentation  
- KPI Creation  
- Trend Analysis  
- Performance Measurement  
- View Creation for Reporting  

All analyses were done using advanced SQL concepts such as **CTEs**, **Window Functions**, **Joins**, **Aggregations**, and **Views**.

---

## 🎯 Business Objectives
1. Analyze time-based sales trends  
2. Evaluate product performance (current vs average vs previous year)  
3. Determine category contribution to total sales  
4. Segment customers into VIP, Regular, and New  
5. Generate customer-level KPIs:  
   - Recency  
   - Average Order Value  
   - Average Monthly Spending  
   - Lifespan  
   - Total Orders / Sales / Quantity  

---


---

## 🧠 SQL Techniques Used
✔ Common Table Expressions (CTEs)  
✔ Window Functions (LAG, SUM OVER, AVG OVER)  
✔ Segmentation & CASE WHEN logic  
✔ Grouping & Aggregations  
✔ Inner & Left Joins  
✔ Ranking & Trend Analysis  
✔ View Creation  
✔ Time-based functions (DATETRUNC, YEAR, MONTH)  

---

# 📈 Analysis Highlights

## **1️⃣ Time-Based Sales Analysis**
- Monthly & yearly trends  
- Total sales, customers, and quantity  
- Useful for seasonality tracking  

---

## **2️⃣ Cumulative & Moving Average Analysis**
- Running totals  
- Moving averages (yearly)  
- Sales trend smoothing  

---

## **3️⃣ Product Performance Analysis**
Compares each product’s:

- Current Year Sales  
- Average Sales  
- Previous Year Sales  
- Above/Below Average Flag  
- Increase/Decrease YoY Flag  

---

## **4️⃣ Category Contribution**
Shows each category’s % contribution to overall business revenue.

---

## **5️⃣ Product Segmentation**
Cost-based segmentation:

- Below 100  
- 100–500  
- 500–1000  
- Above 1000  

---

## **6️⃣ Customer Segmentation**
Based on lifespan + total spend:

- ⭐ **VIP Customers** → ≥ 12 months & > 5000  
- ⭐ **Regular Customers** → ≥ 12 months & ≤ 5000  
- ⭐ **New Customers** → < 12 months  

---

## **7️⃣ Customer Report View**
Created `gold.report_customer` containing:

- Customer Name & Age Group  
- Total Orders, Products, Sales, Quantity  
- Segment (VIP, Regular, New)  
- Recency (months since last order)  
- Average Order Value  
- Average Monthly Spend  
- Customer Lifespan  

---

## 🏗️ How to Run the Project
1. Import CSV files into SQL Server (schema: **gold**)  
2. Run SQL scripts from `/scripts` folder  
3. Execute **Customer Report.sql** to build the reporting view  
4. Query the final dataset:
   ```sql
   SELECT * FROM gold.report_customer;


## 🗂️ Folder StructureRetail-Sales-Insights-SQL/
│
├── datasets/
│   ├── gold.dim_customers.csv
│   ├── gold.dim_products.csv
│   ├── gold.fact_sales.csv
│   ├── gold.report_customers.csv
│   └── gold.report_products.csv
│
├── scripts/
│   ├── Change Overtime Analysis.sql
│   ├── Cumulative Analysis.sql
│   ├── Performance Analysis.sql
│   ├── Part To Whole Analysis.sql
│   ├── Customer Report.sql
│   ├── Segment Products.sql
│   ├── Group Customer Segment.sql
│   ├── Run Query Code.sql
│   └── Script.sql
│
├── documentation/
│   └── Data Analytics Project Docs.docx
│
└── README.md

