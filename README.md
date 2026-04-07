# Vendor-Performance-Analytics
End-to-End ETL and Analytics pipeline for Vendor Performance. Analyzes 12M+ rows using Python & PostgreSQL to optimize procurement and identify inventory risks.

Vendor Performance & Procurement Analytics 📊📌 Project OverviewThis project is an end-to-end data engineering and analytics pipeline designed to analyze over 12 Million rows of retail procurement and sales data. By transitioning from raw CSV files to a structured PostgreSQL database, I developed a modular system to monitor supplier efficiency, profit margins, and inventory risks.



🛠️ Tech Stack
Database: PostgreSQL
Language: Python
Libraries: Pandas, NumPy, SQLAlchemy, Matplotlib, Seaborn
Tools: Jupyter Notebooks, pgAdmin4
Visualisation: Power BI


📂 Project StructureThe project is divided into three modular stages to ensure scalability and clean code:

1_Data_Ingestion.ipynb: A robust ETL script using Python chunksize processing to load 2GB+ of raw data into PostgreSQL without memory overhead.
2_Data_Cleaning.ipynb: SQL-integrated cleaning where I joined multiple tables (Sales, Purchases, Inventory, and Freight), handled null values, and engineered features like Gross Profit and Profit Margin.
3_Vendor_Analysis.ipynb: The final analytical layer containing deep dives into vendor concentration, brand performance, and inventory health.


🚀 Key Business Metrics & AnalysesPareto Analysis (80/20 Rule): 
Visualized supplier concentration to identify the "Strategic Few" vendors who account for the majority of purchase costs.
Profitability Matrix: Segmented vendors by Sales Volume vs. Profit Margin to identify high-revenue/low-margin risks.
Inventory Risk Assessment: Calculated Unsold Inventory levels per vendor to pinpoint capital tied up in slow-moving stock.
ABC Classification: Categorized vendors into A (Strategic), B (Tactical), and C (Transactional) groups based on their cumulative contribution to the business.


📈 Key Insights FoundSupplier Concentration: 
A small group of vendors (e.g., Diageo, Jim Beam) dominates the purchase share, suggesting a need for strong relationship management.
Margin Health: Identified specific brands with high sales but sub-optimal profit margins due to high purchase costs or excise taxes.
Operational Efficiency: Identified vendors with the highest "Unsold Inventory" counts, providing a roadmap for warehouse space optimization.


🔧 Installation & Setup
Clone this repository.
Install dependencies: Bash: pip install -r requirements.txt
Ensure PostgreSQL is running and update the create_engine connection string in the notebooks with your credentials.
Run the notebooks in order: Ingestion → Cleaning → Analysis.

🚧 Future Enhancements:
Interactive Power BI Dashboard for real-time procurement monitoring.
Inventory Turnover Ratio analysis for seasonal trend forecasting.
