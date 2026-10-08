# 📦 DataCo Smart Supply Chain Analytics & Operations Intelligence

[![Python](https://img.shields.io/badge/Python-3.10%20%7C%203.11%20%7C%203.12-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-DataCo%20Supply%20Chain-20BEFF?logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)
[![SQL Queries Verified](<https://img.shields.io/badge/SQL%20Suite-100%25%20Verified%20(65%2F65)-success>)](file:///d:/programming/data_science_project/supply_chain_analytics/04_Advance_sql_analysis.sql)

---

## 📌 Executive Summary

Modern global supply chains operate under tight margins, volatile lead times, and complex multi-tier logistics networks. Without end-to-end data visibility, organizations suffer from untracked delivery delays, margin erosion from loss-making products, and undetected fraudulent transactions.

This project delivers an **end-to-end operational and business intelligence analysis** of DataCo Global's supply chain dataset spanning **180,519 transactions** and **53 features** across 5 global markets (Europe, North America, South America, Asia-Pacific, and Africa).

Using **Python** for rigorous data quality assessment, transformation, and feature engineering, **MySQL** for multi-dimensional business analytics (CTEs, Window Functions, ABC classification, Moving Averages), and **Power BI** for executive dashboarding, this repository provides actionable insights to optimize inventory, enhance on-time delivery, eliminate negative margin leakage, and mitigate transaction fraud.

---

## 🏗️ Analytics Architecture & Pipeline

```text
┌─────────────────────────────────────────────────────────────────────────┐
│                1. RAW DATA INGESTION (Kaggle DataCo API)                │
│                 180,519 Transactions  •  53 Raw Features                │
└────────────────────────────────────┬────────────────────────────────────┘
                                     │
                                     ▼
┌─────────────────────────────────────────────────────────────────────────┐
│             2. DATA CLEANING & VALIDATION (Python / Pandas)             │
│      • Removed 5 redundant attributes (Passwords, URLs, Zip Codes)      │
│      • Datetime normalization & missing value auditing                  │
└────────────────────────────────────┬────────────────────────────────────┘
                                     │
                                     ▼
┌─────────────────────────────────────────────────────────────────────────┐
│               3. FEATURE ENGINEERING (13 Business Metrics)              │
│      • Shipping Duration         • Shipping Performance (On-Time SLA)   │
│      • Profit Category           • Profit Margin Percentage             │
│      • High Value Order          • Sales Quartiles & Weekend Flags      │
└────────────────────────────────────┬────────────────────────────────────┘
                                     │
                                     ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                     4. CLEANED DATASET GENERATION                       │
│              DataCo_Cleaned_Supply_Chain.csv (61 Columns)               │
└──────────────────┬───────────────────────────────────┬──────────────────┘
                   │                                   │
                   ▼                                   ▼
┌─────────────────────────────────────┐ ┌─────────────────────────────────┐
│       PYTHON EXPLORATORY EDA        │ │          MYSQL DATABASE         │
│  • 23 Analytical Visualizations     │ │    dataco_supply_chain_analysis │
│  • Correlation Heatmaps             │ └────────────────┬────────────────┘
│  • Sales & Profit Distributions     │                  │
└─────────────────────────────────────┘                  ▼
                                        ┌─────────────────────────────────┐
                                        │       SQL ANALYTICS SUITE       │
                                        │  • 01: Data Quality & QA        │
                                        │  • 02: Exploratory Aggregations │
                                        │  • 03: Commercial Performance   │
                                        │  • 04: Window Functions, CTEs,  │
                                        │        ABC Analysis & Views     │
                                        └────────────────┬────────────────┘
                                                         │
                                                         ▼
                                        ┌─────────────────────────────────┐
                                        │       POWER BI DASHBOARDS       │
                                        │  • Executive KPI Overview       │
                                        │  • Logistics & SLA Performance  │
                                        │  • Risk, Loss & Fraud Analytics │
                                        └─────────────────────────────────┘
```

---

## 📂 Repository File Structure

| File                                                                                                                                                  |       Type       | Description                                                                                                                                                                      |
| :---------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`DataCo Supply Chain Analytics.ipynb`](file:///d:/programming/data_science_project/supply_chain_analytics/DataCo%20Supply%20Chain%20Analytics.ipynb) | Jupyter Notebook | Complete end-to-end Python pipeline (149 cells, 64 code executions): data loading, cleaning, feature engineering, 23 visualization charts, correlation matrices, and CSV export. |
| [`01_Data_Validation.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/01_Data_Validation.sql)                                 |    SQL Script    | Data governance and quality checks: row counts, missing values, primary key checks, duplicate orders/customers, and value boundary validation.                                   |
| [`02_Exploratory_Data_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/02_Exploratory_Data_Analysis.sql)             |    SQL Script    | High-level business aggregation queries: sales volume, total profit, average order value (AOV), shipping mode distributions, and delivery metrics.                               |
| [`03_Business_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/03_Business_Analysis.sql)                             |    SQL Script    | Granular commercial analytics: top markets, regions, countries, loss-making product identification, customer segment profit, and fraud breakdown.                                |
| [`04_Advance_sql_analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/04_Advance_sql_analysis.sql)                       |    SQL Script    | Production-grade SQL queries using Window Functions (`RANK`, `DENSE_RANK`, `ROW_NUMBER`, `NTILE`), CTEs, 3-month moving averages, running totals, ABC classification, and views. |
| [`requirements.txt`](file:///d:/programming/data_science_project/supply_chain_analytics/requirements.txt)                                             |   Environment    | Locked Python dependencies (`pandas`, `numpy`, `matplotlib`, `seaborn`, `kagglehub`, `SQLAlchemy`, etc.) for seamless reproducibility.                                           |
| [`README.md`](file:///d:/programming/data_science_project/supply_chain_analytics/README.md)                                                           |  Documentation   | Comprehensive project architecture, query guide, findings, and execution instructions.                                                                                           |

---

## 🔬 Feature Engineering Matrix

During the Python pipeline, raw operational data was enriched with **13 new business attributes** to unlock higher-order analysis:

| Engineered Feature         | Logic & Calculation                                          | Business Value                                                           |
| :------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------------------- |
| **`Shipping Duration`**    | `shipping date` − `order date` (in days)                     | Measures actual logistics transit cycle time.                            |
| **`Shipping Performance`** | `Duration <= 3` ➔ `'On Time'`, else `'Delayed'`              | Standardizes operational delivery SLAs across carriers.                  |
| **`Weekend Order`**        | `Order Day Name` ∈ `['Saturday', 'Sunday']`                  | Evaluates consumer weekend purchasing vs. weekday fulfillment load.      |
| **`High Value Order`**     | `Sales >= Median(Sales)` ➔ `'High'`, else `'Regular'`        | Segments transactions for targeted VIP processing.                       |
| **`Sales Category`**       | Tertile split (`pd.qcut(q=3)`) ➔ `['Low', 'Medium', 'High']` | Enables macro sales distribution analysis.                               |
| **`Profit Category`**      | `Order Profit Per Order >= 0` ➔ `'Profit'`, else `'Loss'`    | Flags margin-eroding orders for immediate investigation.                 |
| **`Profit Margin (%)`**    | `(Order Item Profit Ratio) * 100`                            | Normalizes product and order profitability regardless of absolute price. |
| **Calendar Features**      | `Order Year`, `Order Month`, `Quarter`, `Day Name`, etc.     | Unlocks multi-year seasonal and cyclical trend analysis.                 |

---

## 📊 SQL Analytics Suite & Query Catalog

The repository includes a comprehensive 4-part SQL query suite tested and verified against MySQL 8.0+:

### 1. Data Validation & Quality Assurance ([`01_Data_Validation.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/01_Data_Validation.sql))

- Total record count (180,519 rows) and schema inspection.
- Null checks across customer zip codes, delivery statuses, and financial metrics.
- Duplicate order identification (`COUNT(*) - COUNT(DISTINCT Order Id)`).
- Boundary and sanity checks for `Sales`, `Order Profit Per Order`, and distinct counts.

### 2. Exploratory Data Analysis ([`02_Exploratory_Data_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/02_Exploratory_Data_Analysis.sql))

- Global total revenue and gross profit rollups.
- Average Order Value (AOV) and order volume breakdowns.
- Market, country, category, and shipping mode volume distributions.
- Scheduled vs. actual shipping day variances.

### 3. Commercial & Operational Analysis ([`03_Business_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/03_Business_Analysis.sql))

- Revenue and profit contribution across global markets and top 10 countries.
- Identification of top loss-making products (`HAVING total_profit < 0`).
- Customer segment profitability and revenue concentration.
- Suspected fraud distribution segmented by market, shipping mode, and customer type.
- Time-series monthly revenue trends.

### 4. Advanced SQL Engine ([`04_Advance_sql_analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/04_Advance_sql_analysis.sql))

- **Window Functions**:
  - `RANK()` & `DENSE_RANK()`: Ranking top revenue & profit generating products.
  - `ROW_NUMBER() OVER (PARTITION BY Category Name ORDER BY Sales DESC)`: Top 5 products per category.
  - `DENSE_RANK() OVER (PARTITION BY Market ORDER BY Sales DESC)`: Top 3 spenders per global market.
  - `NTILE(4)`: Customer quartile segmentation by purchase volume.
- **Common Table Expressions (CTEs)**:
  - Categories exceeding global average category revenue.
  - Multi-tier customer aggregation.
- **Time-Series Windowing**:
  - **Running Total**: `SUM(monthly_sales) OVER (ORDER BY month)`.
  - **3-Month Moving Average**: `AVG(monthly_sales) OVER (ORDER BY month ROWS BETWEEN 2 PRECEDING AND CURRENT ROW)`.
- **Customer Lifetime Value (CLV)**:
  - Lifetime sales, order frequency, and average basket value per customer.
- **ABC Inventory & Revenue Classification**:
  - **Class A**: Revenue $\ge \$100,000$ (High value, priority supply chain allocation).
  - **Class B**: Revenue $\$50,000$ – $\$99,999$ (Medium value).
  - **Class C**: Revenue $< \$50,000$ (Long tail).
- **Production View & Executive Dashboard**:
  - `vw_sales_summary`: Pre-aggregated view across markets.
  - Executive KPI single-query scorecard.

---

## 💡 Key Business Findings

### 1. Delivery Metric Inconsistencies & Latency

- The dataset tracks late deliveries through two fields: `Late_delivery_risk` (~54.8% flagged) and `Delivery Status` (`'Late delivery'`, `'Advance shipping'`, `'Shipping on time'`, `'Shipping canceled'`).
- Inconsistencies exist between recorded risk flags and delivery statuses, demonstrating that relying on a single indicator without cross-field validation leads to flawed logistics reporting.
- Standard Class accounts for the overwhelming volume of shipments, but experiences the highest absolute count of delays.

### 2. Profitability Leakage & Margin Erosion

- While cumulative business profit is healthy, a notable percentage of individual transactions generate **negative profit**.
- Negative margin orders cluster in specific product lines, heavily discounted orders, and select international shipping destinations where carrier costs outstrip order margins.

### 3. Fraud Clustering Patterns

- Orders flagged as `SUSPECTED_FRAUD` are not evenly distributed; they concentrate heavily in specific geographic markets and payment methods (predominantly `TRANSFER` transactions).
- Consumer segment accounts for the highest fraud attempt frequency, necessitating automated fraud scoring triggers before fulfillment.

### 4. The Pareto Distribution in Sales & CLV

- The top 20% of product catalog items drive over 75% of total gross revenue (Class A products in our ABC model).
- A tightly clustered group of high-frequency customers accounts for a disproportionate share of enterprise revenue.

---

## 🎯 Actionable Business Recommendations

1. **Carrier Contract Renegotiation & Dynamic SLAs**:
   - Re-evaluate carrier tier commitments for Standard Class in markets where late delivery frequency exceeds 50%.
   - Implement real-time dispatch alerts when order-to-shipping transition approaches 3 days.
2. **Discount Guardrails & Margin Protection**:
   - Establish minimum margin floors on high-discount promotions to prevent negative profit transactions.
   - Adjust shipping surcharges on cross-border orders that consistently report negative net profit.
3. **Automated Fraud Prevention Rules**:
   - Implement step-up verification (2FA or manual review) for high-value `TRANSFER` orders originating in flagged high-risk regional markets.
4. **Targeted VIP Customer Retention**:
   - Leverage the Customer Lifetime Value (CLV) model to enroll top quartile customers into proactive loyalty programs with guaranteed fulfillment SLAs.
5. **Inventory Optimization via ABC Classification**:
   - Ensure 98%+ in-stock availability for Class A SKUs while rationalizing or dropshipping low-margin Class C items.

---

## 📈 Power BI Executive Dashboard Suite

The cleaned dataset connects into a multi-page Power BI dashboard designed for executive leadership and logistics directors:

| Dashboard Page                | Core Visualizations                                                                                             | Target Stakeholders                     |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------- | :-------------------------------------- |
| **1. Executive Summary**      | Total Sales, Total Profit, Profit Margin %, AOV, Monthly Sales & Profit Trend, Sales by Market & Category       | C-Suite, VP of Commercial               |
| **2. Logistics Performance**  | On-Time Delivery Rate %, Late Delivery by Shipping Mode, Lead Time by Region, Scheduled vs. Actual Transit Days | VP of Supply Chain, Logistics Directors |
| **3. Risk & Fraud Analytics** | Revenue at Risk, Suspected Fraud by Market & Customer Segment, Loss-Making Order Breakdown by Product           | Operations & Risk Management            |

---

## 🚀 Step-by-Step Setup & How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Tanuj-Narula/supply-chain-analytics.git
cd supply-chain-analytics
```

### 2. Set Up Python Environment

Create and activate a virtual environment, then install all requirements:

```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 3. Acquire the Dataset

You can download the dataset directly via Kaggle or using `kagglehub`:

```python
import kagglehub
path = kagglehub.dataset_download("shashwatwork/dataco-smart-supply-chain-for-big-data-analysis")
print("Dataset downloaded to:", path)
```

Place `DataCoSupplyChainDataset.csv` into the project root directory or note its path.

### 4. Run the Python Notebook

Launch Jupyter Lab or Notebook:

```bash
jupyter lab
```

Open [`DataCo Supply Chain Analytics.ipynb`](file:///d:/programming/data_science_project/supply_chain_analytics/DataCo%20Supply%20Chain%20Analytics.ipynb) and run all cells sequentially. The final cell will generate `DataCo_Cleaned_Supply_Chain.csv`.

### 5. Execute the SQL Scripts (MySQL 8.0+)

1. Create the database in MySQL Workbench or CLI:
   ```sql
   CREATE DATABASE IF NOT EXISTS dataco_supply_chain_analysis;
   USE dataco_supply_chain_analysis;
   ```
2. Import `DataCo_Cleaned_Supply_Chain.csv` into the table `dataco_cleaned_supply_chain` (via MySQL Table Data Import Wizard or `LOAD DATA INFILE`).
3. Run the analysis scripts in order:
   - [`01_Data_Validation.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/01_Data_Validation.sql)
   - [`02_Exploratory_Data_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/02_Exploratory_Data_Analysis.sql)
   - [`03_Business_Analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/03_Business_Analysis.sql)
   - [`04_Advance_sql_analysis.sql`](file:///d:/programming/data_science_project/supply_chain_analytics/04_Advance_sql_analysis.sql)

---

## 🛠️ Tech Stack & Tools

- **Programming & Analysis**: Python (Pandas, NumPy)
- **Data Visualization**: Matplotlib, Seaborn
- **Database Engine**: MySQL 8.0+ (Window Functions, CTEs, Views, Aggregations)
- **Business Intelligence**: Microsoft Power BI
- **Environment & Ingestion**: Jupyter Notebook, KaggleHub API, Git

---
