# 📊 E-commerce Revenue Analysis Dashboard – Power BI + Snowflake

This project analyzes sales and customer behavior for an e-commerce business using Power BI and Snowflake SQL. It provides a comprehensive overview of revenue drivers, top-selling products, customer segmentation, and geographic performance.

---

## 📌 Objective

To identify the key products, customer segments, and countries that drive the most revenue, and to understand business patterns over time through an interactive dashboard.

---

## 🛠️ Tools Used

- **Snowflake** – SQL data extraction and aggregation
- **Power BI** – Data cleaning, transformation (Power Query), dashboard development
- **DAX** – KPI creation and custom measures
- **SQL** – Business logic implementation and metrics extraction

---

## 📊 Key Features

- **Dynamic KPIs**:
  - Total Revenue
  - Units Sold
  - Total Invoices
  - Unique Customers

- **Top Revenue-Generating Products**
- **Revenue by Country**
- **Customer Segmentation (Champions, Loyalists, At-Risk, etc.)**
- **Year-over-Year Transaction Trends**
- **Clean and structured dashboard layout for stakeholder presentation**

---

## 🧠 Business Insights

- 🏆 **Champions** (top repeat customers) generated **76% of total revenue**.
- 🌍 The **United Kingdom** accounted for over **85% of all revenue**, showing heavy geographic concentration.
- 🛍️ The top 3 products alone generated over **$740K in revenue**.
- 🧭 Transaction volume increased **dramatically from 2009 to 2010**, then stabilized.
- ⚠️ Customer segments like **Potential Loyalists** and **At Risk** contributed minimally and may warrant re-engagement strategies.

---

## 🧪 Data Modeling and Snowflake SQL Analysis

The data cleaning, exploratory analysis (EDA), and modeling phase was conducted entirely in **Snowflake SQL** before visualization in Power BI. This ensured the dataset was analysis-ready, consistent, and optimized for aggregation.


- Each raw table contained approximately **520,000 rows** of transactional data.
- Null values were found only in the `Description` and `CustomerID` columns.
- The `Country` column required normalization due to repeated values in different formats.
- The `Description` column included several **non-product transactions** such as gift vouchers, postage, discounts, manual adjustments, and test records.


---

## 🔄 Automation and Refresh Strategy (Simulated)

Although this project uses a static dataset (archived from 2019), its structure was designed to simulate a scalable, production-ready data pipeline.

In a real-world environment, data automation would be implemented depending on business needs and infrastructure:

- **Option A: Live Connection (DirectQuery)**  
  Power BI would connect directly to Snowflake and pull fresh data each time the report is viewed.  
  Ideal for real-time dashboards, frequent updates, or scenarios where stakeholders need the most recent data (e.g., inventory, live sales).  
  This approach ensures live data but may incur higher costs due to more frequent queries and slower performance if not optimized.

- **Option B: Scheduled Refresh (Import Mode)**  
  Power BI would import data from Snowflake and refresh it at scheduled intervals (e.g., daily or weekly) using the Power BI Service.  
  This is a more cost-effective and performant option for dashboards where near-real-time data isn't required.  
  Businesses often choose this approach when data latency of a few hours is acceptable.

This project demonstrates the upstream logic typically required for either approach:

- **Data Cleaning and Modeling** were performed in both **Snowflake SQL** and **Power BI**.  
  - In Snowflake, raw data from two separate years was cleaned and merged into a unified **fact table** using SQL.  
  - Business logic such as revenue calculation (`quantity * unit_price`) was implemented both upstream (SQL) and in Power BI using DAX.

- **Dynamic Filters and Interactivity** were built into the Power BI dashboard, enabling simulated real-time exploration by country, segment, and product.

While actual automation was not implemented due to the static nature of the dataset, the pipeline design reflects best practices for scalable enterprise analytics.

---

## 📁 Folder Structure

/SQL → Snowflake SQL queries  
/Dashboard → Power BI .pbix file + dashboard screenshot  
/Data → (Optional) Cleaned .csv files or mock data  
/README.md → Project documentation


---

## 📸 Dashboard Preview

> <img width="2025" height="1059" alt="Screenshot 2025-08-07 052951" src="https://github.com/user-attachments/assets/0eeadb7e-0841-4c7c-85a7-2a8e2e6bceee" />


---

## 📩 Contact

If you're a recruiter, hiring manager, or fellow analyst and would like to collaborate or learn more, feel free to reach out via [LinkedIn](www.linkedin.com/in/miguel-negron-garcia-3a6b001b9).

