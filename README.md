
## Data Warehouse Analytics Project
This repository features a complete SQL-based data warehousing solution, transitioning raw transactional data into a refined Gold Layer for business intelligence. The project demonstrates end-to-end database engineering, from schema architecture and data ingestion to advanced analytical reporting.

🏗️ Architecture & Design
The system is built on a Star Schema within the DataWarehouseAnalytics database:

Gold Schema: A dedicated layer for clean, reporting-ready data.

Dimension Tables: dim_customers and dim_products store descriptive attributes like demographics and product categories.

Fact Table: fact_sales captures quantitative transaction data, including sales amounts and quantities.

# 🛠️ Technical Implementation
Data Pipeline: Automated data loading from flat files using BULK INSERT with high-performance configurations like TABLOCK.

Advanced SQL: Leverages Common Table Expressions (CTEs) and Window Functions (SUM OVER, AVG OVER, LAG) to calculate complex metrics.

Time-Series Analysis: Uses DATETRUNC and FORMAT to analyze sales trends across months and years.

# 📊 Business Intelligence & Reporting
The project concludes with two modular SQL Views designed to provide 360-degree insights:

1. Customer Report (gold.report_customers)
Segmentation: Classifies customers as VIP, Regular, or New based on their spending and 12-month loyalty lifespan.

Demographics: Groups customers into age brackets (e.g., 20-29, 30-39) to identify core audiences.

Key KPIs: Tracks Recency (months since last order), Average Order Value (AOV), and Lifespan.

2. Product Report (gold.report_products)
Performance Ranking: Segments products into High-performer, Mid-Range, and Low-Performer based on total revenue.

Inventory Insights: Analyzes product maintenance, costs, and average selling prices.

Revenue Metrics: Calculates average monthly revenue and order-level profitability.

# 🚀 How to Use
Execute the SQLQuery1.sql script in SQL Server Management Studio (SSMS).

Update the file paths in the BULK INSERT statements to match your local directory.

Query the gold.report_customers and gold.report_products views for instant business insights
