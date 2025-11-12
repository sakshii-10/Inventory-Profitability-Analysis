# Inventory-Profitability-Analysis
End-to-end project leveraging Python, PostgreSQL, Statistical T-Tests, and Power BI to validate and visualize vendor profitability drivers.
# Vendor Performance Optimization & Profitability Analysis

## Project Overview

This project implements a complete Data Analytics pipeline to analyze a large-scale `vendor_sales_summary` dataset. The primary goal is to move beyond descriptive statistics and use rigorous **statistical validation** to identify and quantify the impact of high-performing vendors on overall profitability. The final deliverable is an interactive Power BI dashboard for strategic business decision-making.

## Key Goals & Impact

- **Optimize Data Ingestion:** Achieve high-speed, robust loading of massive datasets into PostgreSQL.
- **Statistical Rigor:** Use hypothesis testing to statistically prove the difference in profitability across vendor tiers.
- **Actionable Insights:** Translate complex data and statistical results into clear, interactive business intelligence.

## Technical Stack

- **Data Engineering:** Python (Pandas), Psycopg2
- **Database:** PostgreSQL (Optimized `COPY` command)
- **Statistical Analysis:** Python (SciPy - Two-Sample T-Test)
- **Business Intelligence (BI):** Power BI (`Vendor_Performance.pbix`)

## Project Pipeline & Files

### 1. Data Load & Exploration (`Data Load and Exploration (1).ipynb`)
* **Methodology:** Demonstrates an advanced, memory-efficient method for data ingestion using Python's `io` module combined with the PostgreSQL `COPY` command, resulting in significantly faster loading times compared to standard SQL `INSERT` operations.
* **Output:** The `vendor_sales_summary` dataset is cleaned, transformed, and efficiently loaded into the PostgreSQL database.

### 2. Exploratory Data Analysis (EDA) & Statistical Validation (`EDA with Python.ipynb`)
* **Methodology:** Performs key feature engineering to calculate metrics like `Profit Margin` and `Total Sales Dollars`.
* **Statistical Core:** Implements a **Two-Sample T-Test (Welch's)** to test the hypothesis: *Is there a statistically significant difference in profit margins between top-performing and low-performing vendors?*
* **Result:** The analysis provides a P-value and T-statistic, offering statistical proof for the observed profitability gap.

### 3. Business Intelligence Dashboard (`Vendor_Performance.pbix`)
* **Deliverable:** A fully interactive Power BI report that visualizes vendor performance against key financial metrics (Profit Margin, Total Sales, etc.).
* **Purpose:** Allows stakeholders to filter, drill down, and understand the statistically validated findings to guide vendor management and procurement strategy.
