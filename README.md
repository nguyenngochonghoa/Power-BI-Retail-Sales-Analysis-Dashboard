# Retail Sales Analysis Dashboard (Power BI)

## 📌 Project Overview
This project presents an interactive Power BI dashboard for analyzing retail sales performance.  
The dashboard helps stakeholders monitor business KPIs, identify sales trends, and evaluate product performance across multiple dimensions such as time, region, channel, category, and manufacturer.

The dashboard is structured into three pages for different levels of analysis:  

- **Overview** → Business-wide KPIs and trends  
- **Product Analysis** → Performance across categories, segments, sold/unsold status  
- **Product Details** → In-depth product-level insights  

---

## 🎯 Problem Statement
In a competitive retail environment, businesses need more than just raw transactional data. They require a centralized and visualized reporting system to answer key questions such as:  

- How are revenue and sales units performing over time?  
- Which regions, channels, and manufacturers drive the most growth?  
- Which products are top sellers, and which remain unsold?  
- What is the performance of different categories and segments?  
- How can managers make informed decisions to optimize product portfolio and sales strategy?  

This dashboard bridges the gap between raw data and actionable insights, enabling better decision-making for managers and product teams.

---

## Dataset
The dataset contains retail sales transactions with the following information:

- **Sale:** product_id, date, zip, units, revenue, sales_channel
- **Geo:** zip, city, state, region, district
- **Channel:** channel_id,	channel
- **Product:** product_id, name, category, segment, manufacturer_id  
- **Manufacturer:** manufacturer_id, name

---

## Dashboard Design

### 🔹 Page 1: Overview
**KPIs:** Revenue, Units Sold, Avg Revenue per Unit, Orders, Avg Order Value  

**Charts:**  
- Revenue & Units Sold by Year-Month  
- Revenue & Units Sold by Region  
- Revenue & Units Sold by Channel  
- Revenue & Orders by Manufacturer  
- Revenue & Units by Region & Channel  

**Slicers:** Date, Location, Channel, Manufacturer  

### 🔹 Page 2: Product Analysis
**KPIs:** Total Products, Top Selling Product  

**Charts:**  
- Revenue by Quarter & Category/Segment/Channel  
- Product Sales Status (Sold vs Unsold)  
- Top/Bottom N by Unit Sold  
- Unsold Products by Segment/Category  
- Sales Performance by Segment (scatter/bubble)
- List of Unsold Products 

**Table:** List of Unsold Products (with search filter)  

**Slicers:** Date, Location, Channel, Category, Segment, Product Name

### 🔹 Page 3: Product Details
**Table:** Product Information (ID, Name, Manufacturer, Segment, Category, Orders, Revenue, Units, ARPU, AOV)  

**Slicers:** Date, Location, Channel, Category, Segment, Manufacturer, Product Name  

---

## Tech Stack
- **Tools Used**: Power BI Desktop, Power Query (M Language), DAX.
- **Data Modeling**: Created a star-schema data model with established relationships between fact and dimension tables.
- **DAX Measures**: Developed complex measures for:
  - KPI Calculation (Revenue, AOV, ARPU, etc)
  - Ratio Analysis (Unsold Products %)
- **Data Transformation**: Used Power Query for data cleaning, shaping, and building a robust ETL pipeline.

---

## 📈 Key Insights

### 1. Business Performance (Overview Page)
- Total Revenue reached **$213M**, with **118K units sold**, demonstrating a large-scale and efficient business model.  
- Average Order Value (AOV) stands at **$1.85K**, reflecting high-value transactions.  

**Seasonality in Sales:**  
- Strong growth in Jan 2024 ($21.3M) and Nov 2024 ($24.9M)  
- Weak performance in mid-year, lowest in Jul 2024 ($9.9M) before recovery  

**Sales Channels:**  
- Online (35.18%) and Outlet (35.16%) are main revenue drivers  
- Stores contribute moderately (24.95%)  
- Social Media underperforms (4.7% of revenue)  

**Regional Insights:**  
- East dominates: $97M revenue, 52K orders  
- West: $60M, 33K orders  
- Central: $56M, 30K orders  

**Manufacturers:**  
- Performance concentrated in key players: B&H Photo Video ($68M, 41K orders)  
- Others like Sam’s Club, Amazon, Staples, Target contribute minimally  

### 2. Product Analysis (Product-Level Insights)
- **Top Product:** Ring Video Doorbell 4 – $11.8M revenue (+11.3% MoM), 6.7K units sold  
- **Product Portfolio:** 2.4K SKUs, only 28.15% sold, 71.85% remain unsold  

**Unsold Products SKUs:**  
- **By Category:** Urban (938) & Rural (504) dominate inventory backlog  
- **By Segment:** Productivity (392) & Convenience (257) highest unsold counts  

**Segment Performance:**  
- Productivity: core segment, $86.8M revenue, 48.7K units  
- Extreme: fewer units (13.2K) but highest revenue/unit ($1.8K+), total $24.4M  
- Moderation, Select, Youth: mid-level performance  
- Regular, All Season: weakest contributors  

### 3. Strategic Takeaways
- East region should remain the primary market focus  
- Online & Outlet channels are growth engines; Social Media needs improvement  
- High inventory of unsold products, especially Urban & Productivity categories  
- Productivity and Extreme segments are most profitable  
- Portfolio optimization needed: discontinue or revamp underperforming SKUs  

---

## How to Use
1. Open the `.pbix` file in Power BI Desktop  
2. Use the slicers (Date, Location, Channel, Manufacturer, etc.) to filter the data dynamically  
3. Navigate across the three pages to explore insights at overview, group analysis, and product detail levels  
