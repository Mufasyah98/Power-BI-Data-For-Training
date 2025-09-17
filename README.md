[Slide](https://drive.google.com/file/d/1F1wYcm0K9ry46RFHg--_-_N5ZioeBssR/view?usp=sharing)

# RetailMart Power BI Case Study

## 📌 Overview
**RetailMart** is a large UK-based retail chain operating multiple stores nationwide.  
This case study simulates a **real-world Power BI project**, allowing you to practice data cleaning, modeling, and dashboard creation using realistic datasets for sales, marketing, customers, products, stores, and more.

The objective is to create a **centralized, interactive dashboard** to monitor:
- Sales Performance
- Customer Insights
- Product Profitability
- Marketing Effectiveness
- Sales Team Performance

---

## 📂 Datasets Included
| Dataset | Description |
|---------|-------------|
| `sales_data_2022.csv` | Sales transactions for 2022 (16,783 records) |
| `sales_data_2023.csv` | Sales transactions for 2023 (15,856 records) |
| `sales_data_2024.csv` | Sales transactions for 2024 (17,314 records) |
| `products_table.csv` | Product details including price, cost, category, brand, and supplier |
| `categories_table.csv` | Category ID and category names |
| `salespersons_table.csv` | Salesperson demographics, hire date, region, and salary |
| `customers_table.csv` | Customer demographics, address, loyalty points, and preferred payment |
| `stores_table.csv` | Store details including location (latitude/longitude), type |
| `marketing_spend_table.csv` | Marketing campaigns, spend, conversion rates, ROI |
| `malaysia_public_holidays_2022_2024.csv` | Public holidays for seasonality analysis |

---

## 🎯 Business Questions
The dashboards should help answer:

### **Sales Performance**
- What are the total sales and profit for each year from 2022 to 2024?
- Which product categories are growing/declining YoY?
- Which stores are over/under-performing compared to the average?

### **Customer Insights**
- Who are the top customers by spending?
- What is the distribution of customers by region and segment?
- Which payment methods are most popular per region?

### **Product & Profitability**
- Which products have the highest profit margins?
- Which brands dominate sales revenue?
- How does supplier performance impact profitability?

### **Marketing Effectiveness**
- Which channels have the best ROI?
- How does marketing spend relate to sales growth?
- Which campaigns achieved the highest conversion rates?

### **Sales Team**
- Which salespeople generate the most revenue?
- How does salesperson tenure impact sales performance?

---

## 🛠 Tasks
1. **Data Preparation**
   - Import datasets into Power BI
   - Clean and transform data using Power Query
   - Create relationships using a **star schema**

2. **Data Modeling**
   - Create DAX measures:
     ```DAX
     Total Sales = SUMX(Sales, Sales[Quantity Sold] * RELATED(Products[Price Per Unit]))
     Total Profit = SUMX(Sales, (RELATED(Products[Price Per Unit]) - RELATED(Products[Cost Per Unit])) * Sales[Quantity Sold])
     Profit Margin % = DIVIDE([Total Profit], [Total Sales])
     ```
   - Calculate YoY growth and marketing ROI

3. **Visualization**
   - **Sales Overview Dashboard** – KPIs, trends, maps, category performance
   - **Customer Insights Dashboard** – Demographics, loyalty points, segments
   - **Marketing & Sales Team Dashboard** – Spend vs revenue, salesperson leaderboard

4. **Advanced Features**
   - Add slicers for Year, Region, Store Type, Product Category
   - Use conditional formatting for performance thresholds
   - Include a decomposition tree for profit drivers

5. **Publishing**
   - Publish to Power BI Service
   - Apply Row-Level Security (RLS) for region managers
   - Schedule daily data refresh

---

## 📊 Expected Dashboards
- **Dashboard 1: Sales Overview**
  - KPIs: Total Sales, Total Profit, Profit Margin %, YoY Growth
  - Monthly sales trend (Line Chart)
  - Sales by category (Bar Chart)
  - Store location sales map

- **Dashboard 2: Customer Insights**
  - Customer segment analysis
  - Loyalty program leaderboard
  - Preferred payment method breakdown

- **Dashboard 3: Marketing & Sales Team**
  - Marketing channel ROI comparison
  - Campaign performance
  - Salesperson ranking

---

## 🎓 Learning Outcomes
By completing this case study, you will:
- Gain proficiency in **Power Query** for data cleaning
- Understand **data modeling** and star schema relationships
- Write **DAX** for KPIs and advanced calculations
- Build **interactive dashboards** for multiple business areas
- Integrate **geographic data** for mapping insights
- Measure **marketing ROI** and **sales team performance**

---

## 🖼 Company Logo
![RetailMart Logo](<img width="1024" height="1024" alt="Logo Retail" src="https://github.com/user-attachments/assets/f1ad1b5c-c7ae-4d46-a4bd-7ef08172ccba" />
)

---

## 📥 Download Data
All datasets are included in the `data/` folder of this repository.

---

## 📄 License
This case study is for **educational and training purposes only**.
