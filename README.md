# 🛍️ Smart Store Business Intelligence Dashboard

This repository contains a complete end-to-end **Business Intelligence (BI) project** built using a real-world simulated e-commerce dataset from the *Smart Store*. The goal of the project was to clean, model, query, and visualize transactional data in order to uncover **actionable business insights** for executive decision-making.

📊 Created as part of my **Data Analytics Internship**, this project showcases my ability to work across the entire data pipeline — from raw CSV files to an interactive Power BI dashboard.

---

## 🔧 Tech Stack

- **Python (Google Colab)** – data cleaning and transformation  
  → Libraries: `pandas`, `numpy`  
- **SQL Server Management Studio (SSMS)** – relational database creation & querying  
- **Power BI Desktop & Power BI Service** – data modeling & dashboard creation  
- **DAX** – for advanced KPIs and visual logic  

---

## 🔄 Project Workflow

This project followed a complete **data analytics lifecycle**, from raw data to actionable insights:

### 1. **Data Cleaning & Transformation (Python – Google Colab)**
- Loaded a large e-commerce dataset with 27 raw fields.
- Identified and resolved anomalies:
  - 16 null values in `product_base_margin`
  - 12 products with multiple base margins
  - 2 products with multiple unit prices
  - 3 orders with conflicting order priorities
- Cleaned and normalized the dataset using `pandas` and `numpy`.
- Split the data into six logical tables: `orders`, `order_items`, `products`, `customers`, `locations`, `managers`.
- Exported the cleaned tables as `.CSV` files.

### 2. **Relational Database Creation (SQL Server Management Studio)**
- Created a normalized relational schema with proper **primary** and **foreign keys** (see ERD below).
- Imported all cleaned `.CSV` files into SQL Server.
- Wrote complex SQL queries to explore the data and prepare for dashboard metrics:
  - Aggregations
  - Joins
  - Profitability analysis
  - RFM pre-processing
- Validated data integrity and relationships.

### 3. **Dashboard Development (Power BI Desktop + Service)**
- Imported relational model from SQL Server into Power BI.
- Built a **multi-tab, interactive dashboard** with:
  - KPIs (Total Sales, Profit, MoM Growth)
  - Advanced DAX measures
  - Hierarchical drill-throughs
  - RFM segmentation
  - Interactive maps, pie/ribbon/race charts, and scatter plots
  - **Filters pane on every page** for dynamic slicing by product, region, and time
- Organized dashboard into 8 tabs for ease of navigation.

### 4. **Final Deliverables**
- Published the dashboard via Power BI Service (for personal use).
- Created a short **presentation** to explain dashboard structure and insights.
- Prepared `.pbix` file and tab screenshots for version control and portfolio.

---

## 🧱 Data Model (ERD)

The dataset was normalized into six interrelated tables for easier querying and analysis:

![Data Model](model.PNG)

1. **Orders**: Order-level data (ID, date, priority, return status)  
2. **Order Items**: Transactional line items, with all financial fields (sales, profit, shipping, etc.)  
3. **Products**: Product catalog with category, sub-category, and pricing data  
4. **Customers**: Customer ID, name, and segment  
5. **Locations**: Geographic data (city, state, postal code, region)  
6. **Managers**: Region-wise manager assignments

---

## 📈 Dashboard Overview

> Built in **Power BI**, the dashboard consists of **8 interactive tabs** designed for CEOs, analysts, and marketing teams.

### 1. **Overview**
- KPIs: Total Profit, Sales, Orders, Returns, Customers
- MoM Sales and Profit Growth (vs. goal)
- Profit vs. Units Sold over time
- Revenue by state (Filled Map)
- Best/Worst performing products by profit

### 2. **Products**
- Pie chart: Product category breakdown
- Profit margin analysis (category-wise)
- Profit over time (Ribbon Chart)
- Drill-through: Sub-category view with scatter plot & subcategory margin insights

### 3. **Distribution**
- Bubble map: Sales and Profit by state
- Highest/Lowest state cards
- Column chart: Profit by Region
- Waterfall chart: Profit over time by State/City
- Race chart: State-wise sales trends

### 4. **Customers**
- KPIs: Total Customers, Repeat Purchase %
- Segment-wise breakdown (Corporate, Home Office, Consumer, Small Business)
- Line chart: Monthly First-Time Buyers
- **RFM Analysis**:
  - Clusters: New/Promising, Churned, Core Revenue Drivers, At Risk, Watchlist
  - Deep segmentation by recency, frequency, and monetary value

### 5. **Shipping**
- Average shipping days by state (Filled Map)
- Ship mode & priority breakdown
- Shipping speed vs. priority/mode

### 6. **Returns**
- Total returns and return rate
- Profit loss/gain due to returns
- Return trends over time
- Return rates by region and state

### 7. **Discounts**
- Discounted vs. undiscounted item analysis
- Profit margin by discount group
- Discount group breakdown by product category

### 8. **Orders**
- Cleaned, raw transactional data table



### 🎛️ Universal Filters Pane

Every page includes a **filters pane** with slicers for seamless interactivity.  
Users can slice visualizations by:

- **Product Category & Sub-Category**
- **Timeline / Date Range**
- **US Region, State, and City**

This design enables fast exploration and **targeted insights** based on business questions.

---

## 📌 Key Takeaways

- 🎯 Built a clean, normalized relational model from a messy raw dataset.
- 🧠 Designed strategic KPIs and DAX calculations for MoM growth, customer segmentation, and margin analysis.
- 🧭 Provided insights into product performance, customer behavior, return trends, and discount effectiveness.
- 🚀 Delivered a professional Power BI dashboard suitable for executive stakeholders.

---

## 📝 License

This project is licensed under the **MIT License**.

---

> 📌 **Note**: Screenshots of each tab and the `.pbix` file will be uploaded to this repository. The Power BI Service version is not public at this time.
