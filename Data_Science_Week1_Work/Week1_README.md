# Data Science Internship --- Week 1

## Project Overview

This repository contains the completed Week 1 Data Science Internship
assignment. The work covers three connected parts of a practical data
workflow:

1.  **Data Cleaning & Preprocessing**
2.  **Sales Data Analysis**
3.  **Data Visualization & Dashboarding**

The project focuses on preparing reliable data, calculating business
KPIs correctly, identifying evidence-based sales and customer patterns,
and communicating the results through a Power BI dashboard and final
analytical report.

## Tasks

### Task 1 --- E-Commerce Dataset Cleaning

The customer shopping behavior dataset was inspected, cleaned,
validated, and prepared for analysis.

Key steps:

-   Inspected dataset structure, data types, and summary statistics.
-   Measured missing values.
-   Imputed 37 missing `review_rating` values using the median rating
    within each product category.
-   Standardized column names to lowercase `snake_case`.
-   Checked numerical fields for invalid values.
-   Checked categorical fields for whitespace inconsistencies.
-   Investigated duplicate records.
-   Removed the redundant `promo_code_used` column after confirming it
    duplicated `discount_applied`.
-   Created `age_group` and `purchase_frequency_days`.
-   Saved the cleaned dataset separately while preserving the raw source
    data.

**Final cleaned dataset:** 3,900 rows × 19 columns, with 0 missing
values and 0 fully duplicated rows.

### Task 2 --- Sales Data Analysis

The Sample Superstore dataset was analyzed to evaluate sales
performance, trends, products, regions, and customer behavior.

The source contains 9,994 order-line records. Because one order can
contain multiple products, order-based metrics use **unique `order_id`
values** rather than row counts.

#### Core KPIs

  -----------------------------------------------------------------------
  KPI                                                              Result
  ------------------------------ ----------------------------------------
  Total Revenue                                            \$2,297,200.86

  Total Orders                                                      5,009

  Average Order Value                                            \$458.61

  Total Units Sold                                                 37,873

  Top-Selling Category                                         Technology

  Top Revenue-Generating Product    Canon imageCLASS 2200 Advanced Copier
  -----------------------------------------------------------------------

Additional analysis covers yearly/monthly sales trends, category and
product performance, regional performance, customer behavior, repeat
customers, customer segments, and evidence-based business questions.

### Task 3 --- Power BI Visualization Challenge

A one-page Power BI dashboard was created using the same Sample
Superstore dataset analyzed in Task 2.

The dashboard includes:

-   Total Revenue, Total Orders, Average Order Value, and Total Units
    Sold KPI cards
-   Revenue by Category
-   Monthly Sales Trend
-   Revenue Share by Customer Segment
-   Top 10 Products by Units Sold
-   Revenue by Region
-   Year, Region, Category, and Segment slicers

## Key Findings

-   Approximately **\$2.30 million** in revenue was generated from
    **5,009 unique orders** and **37,873 units sold**.
-   Revenue declined approximately **2.83% in 2015**, then increased
    approximately **29.47% in 2016** and **20.36% in 2017**.
-   **November 2017** recorded the highest monthly revenue at
    approximately **\$118,448**.
-   **Technology** was the highest-revenue category at approximately
    **\$836,154 (36.40%)**.
-   The **Canon imageCLASS 2200 Advanced Copier** led product revenue,
    while **Staples** led unit volume.
-   The **West** generated the highest regional revenue at approximately
    **\$725,458 (31.58%)**.
-   The **Consumer** segment generated approximately **50.56%** of total
    revenue.
-   **781 of 793 customers (98.49%)** were repeat customers and
    generated approximately **99.78%** of observed revenue.

## Business Recommendations

-   Evaluate retention and repeat-purchase initiatives because repeat
    customers account for most observed revenue.
-   Investigate the factors associated with stronger sales in 2016--2017
    before attributing the increase to a specific cause.
-   Evaluate products using both revenue and unit volume.
-   Maintain attention on Technology while preserving the contribution
    of Furniture and Office Supplies.
-   Investigate regional differences using profitability, customer
    density, product mix, and order characteristics.
-   Consider customer-segment differences when evaluating merchandising
    and customer-engagement strategies.

These are potential actions based on observed patterns, not causal
conclusions.

## Tools & Technologies

-   Python
-   Pandas
-   Jupyter Notebook
-   Power BI
-   Matplotlib

## Repository Structure

``` text
Data-Science-Week-1/
├── data/
│   ├── raw/
│   │   ├── customer_shopping_behavior.csv
│   │   └── Sample - Superstore.csv
│   └── cleaned/
│       └── customer_shopping_behavior_cleaned.csv
├── notebooks/
│   ├── Task1.ipynb
│   └── Task2.ipynb
├── outputs/
│   ├── charts/
│   └── dashboard/
│       └── Task3_Dashboard.pbix
├── reports/
│   └── final_report.pdf
├── screenshots/
│   ├── dataset-overview.png
│   ├── missing-values-report.png
│   ├── sales-kpi-summary.png
│   ├── monthly-sales-trend.png
│   └── dashboard-mockup.png
├── presentation/
│   └── Week1_Team_Presentation.pptx
├── README.md
└── requirements.txt
```

## How to Run the Project

1.  Clone or download the repository.
2.  Install dependencies with `pip install -r requirements.txt`.
3.  Open the notebooks in Jupyter Notebook, JupyterLab, or VS Code.
4.  Run `notebooks/Task1.ipynb` from top to bottom.
5.  Run `notebooks/Task2.ipynb` from top to bottom.
6.  Open `outputs/dashboard/Task3_Dashboard.pbix` in Microsoft Power BI
    Desktop.
7.  See `reports/final_report.pdf` for the consolidated report.

> Before final submission, notebook data-loading paths should use
> repository-relative paths matching the structure above.

## Analytical Assumptions and Limitations

-   The Task 1 customer-shopping dataset and Task 2/3 Sample Superstore
    dataset are separate datasets.
-   Sample Superstore is stored at the order-line level; unique Order ID
    is used for order-based metrics.
-   Revenue is calculated from the supplied `Sales` field.
-   Repeat customers are customers with more than one unique order in
    the supplied dataset.
-   The analysis identifies patterns but does not establish causal
    explanations for sales changes.
-   Conclusions are limited to the supplied datasets and their
    represented time periods, customers, products, and geography.

## Deliverables

The repository contains the cleaned dataset, Task 1 cleaning notebook,
Task 2 analytical notebook, Power BI dashboard, supporting screenshots,
final report, team presentation, README, and dependency file.
