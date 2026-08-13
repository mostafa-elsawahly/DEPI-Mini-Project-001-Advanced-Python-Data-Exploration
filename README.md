
# Superstore Retail Analytics & Automated Reporting

**Author:** Mostafa Elsawahly
**Project:** Mini-Project-001 | Advanced Python Data Exploration

## Business Scenario

A multinational retail company required an automated analytical solution to monitor sales, profitability, customer behavior, and operational performance. This project delivers a comprehensive end-to-end data pipeline, transforming raw retail data into actionable business insights using advanced Python programming.

## Key Business Questions Answered

1. **Seasonality:** What is the monthly seasonality of order volumes and sales throughout the year?
2. **Category Performance:** Which product categories generate the highest profit margins, and which are underperforming?
3. **Regional Deficits:** Why is the Furniture category causing significant financial losses specifically in the Central region?
4. **Discount Impact:** What is the statistical correlation between applied discounts and overall profitability?
5. **Logistics Efficiency:** How does the choice of shipping mode impact the average shipping duration (in days)?
6. **Geospatial Distribution:** Which US states contribute the highest and lowest to overall operational profit?
7. **Customer Value:** Who are the Top 10 most valuable customers based on their lifetime monetary contribution (RFM Segmentation)?
8. **Operational Peaks:** Which days of the week experience the highest frequency of customer orders?
9. **Volume vs. Profit:** Does a higher order quantity mathematically correlate with increased financial returns?
10. **Pricing Strategy:** How do different discount buckets (Low, Medium, High) directly affect the average profit per transaction?

## Technical Stack

* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Data Storage Optimization:** PyArrow (Parquet)
* **Visualization:** Matplotlib, Seaborn, Plotly Express
* **Environment:** Jupyter Notebook / VS Code

## Project Workflow & Key Features

### 1. Data Cleaning & Preprocessing

* Handled missing values (e.g., automated imputation for Postal Codes).
* Ensured data type consistency and resolved implicit structural errors.
* Implemented robust exception handling (`try...except`) for file operations and dynamic data ingestion.

### 2. Feature Engineering

* Developed calculated metrics: `Profit Margin`, `Shipping Duration (Days)`, and `Discount Buckets`.
* Extracted temporal dimensions for seasonality analysis: `Order Month`, `Order Weekday`.

### 3. Exploratory Data Analysis (EDA) & Visualization

* **Time-Series Analysis:** Mapped out weekly and monthly sales seasonality to identify peak operational periods.
* **Geospatial Mapping:** Generated interactive choropleth maps tracking profit distribution across US states.
* **Profitability Diagnostics:** Isolated critical financial drains, specifically pinpointing significant losses within the Furniture category in the Central region.
* **Logistics Analysis:** Correlated shipping modes with average profit margins and delivery times.
* **Statistical Correlation:** Executed a comprehensive correlation matrix (Heatmap) to evaluate the mathematical relationships between numeric variables (Sales, Profit, Discount, Quantity).

### 4. RFM Customer Segmentation

* Engineered an RFM (Recency, Frequency, Monetary) model.
* Successfully identified and visualized the Top 10 most valuable customers based on lifetime monetary contribution.

### 5. Memory Optimization & Automated Handoff

* Transitioned from standard CSV/Excel outputs to columnar `Parquet` format, drastically reducing memory footprint and read/write times for downstream reporting.
* Automated the export of cleaned analytical datasets to a dedicated `handoff_data` directory.

## How to Run the Project

1. Ensure all dependencies are installed (`pip install pandas matplotlib seaborn plotly pyarrow numpy`).
2. Run the notebooks in the following sequential order to replicate the pipeline:
   * `cleaning_data.ipynb`
   * `feature_engineering_analysis.ipynb`
   * `visualization_dashboard.ipynb`
3. Check the `handoff_data` folder for the exported Parquet files and automated summaries.
