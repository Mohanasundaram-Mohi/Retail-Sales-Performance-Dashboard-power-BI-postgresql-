# 📊 Retail Sales Performance Dashboard (Power BI Project)

## 🔎 Project Overview

This project showcases an end-to-end **Retail Sales Analysis Dashboard** built using **Power BI** and **PostgreSQL**.
The goal of this project is to transform raw transactional data into meaningful insights that help understand sales performance, customer behavior, and product trends.

The dashboard answers key business questions using interactive visuals and DAX-based calculations.

---

## 🛠 Tools & Technologies

* PostgreSQL (pgAdmin4) – Data storage & SQL analysis
* Power BI Desktop – Data visualization & dashboard creation
* SQL – Business problem solving
* DAX – Calculated columns and measures
* GitHub – Project version control

---

## 📂 Dataset

The dataset contains retail sales transaction data with the following fields:

* Transaction ID
* Sale Date & Time
* Customer ID
* Gender & Age
* Product Category
* Quantity Sold
* Price per Unit
* COGS
* Total Sale

---

## 📊 Dashboard Features & Insights

### ✅ Sales Analysis

* Total sales by product category
* Monthly sales trend analysis
* High-value transactions (>1000)

### ✅ Customer Insights

* Top 5 customers based on total sales
* Unique customers per category
* Average age of customers (Beauty category)

### ✅ Operational Insights

* Transactions by gender & category
* Shift-wise order distribution (Morning, Afternoon, Evening)
* Daily sales view for Nov 05, 2022

---

## 📈 Visualizations Included

* KPI Cards
* Clustered Column Charts
* Donut Chart
* Bar Chart (Top Customers)
* Line/Column Chart (Monthly Sales Trend)
* Table Visuals with filters
* Shift-wise Order Analysis

---

## 🧠 DAX Calculations Used

```DAX
Total Sales = SUM(retail_sales[total_sale])

Total Orders = COUNT(retail_sales[transactions_id])

Unique Customers = DISTINCTCOUNT(retail_sales[customer_id])

Avg Age = AVERAGE(retail_sales[age])

Shift = 
SWITCH(
    TRUE(),
    HOUR(retail_sales[sale_time]) <= 12, "Morning",
    HOUR(retail_sales[sale_time]) <= 17, "Afternoon",
    "Evening"
)
```

---

## 📌 Key Findings

* Electronics and Clothing categories generated the highest sales
* Evening shift recorded the maximum number of orders
* Monthly analysis highlighted peak sales months across years
* A small group of customers contributed significantly to revenue
* Customer distribution across categories remained balanced

---

## 🚀 How to Use This Project

1. Connect PostgreSQL database to Power BI
2. Load the retail_sales table
3. Create calculated columns and DAX measures
4. Build visuals and apply filters
5. Explore insights using the interactive dashboard

---

## 👨‍💻 Author

**Mohan**
This project is part of my data analytics portfolio demonstrating SQL and Power BI skills.
I’m open to feedback, collaboration, and learning opportunities.

---

⭐ If you found this project useful, feel free to star the repository!
