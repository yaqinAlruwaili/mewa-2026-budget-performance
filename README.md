# MEWA | 2026 Budget Performance Dashboard

## Project Overview

This project presents an interactive Power BI dashboard analyzing the 2026 budget performance of the **Ministry of Environment, Water and Agriculture (MEWA), Saudi Arabia**.

The dashboard provides an executive-level overview of budget allocations, cumulative spending, budget execution rates, remaining budget, and budget adjustments across five expenditure categories.

The objective is to transform government open data into clear financial insights that support budget monitoring and data-driven decision-making.

## Business Objectives

- Monitor original and current budget allocations.
- Track cumulative spending and budget execution rates.
- Identify expenditure categories with high budget utilization.
- Analyze budget adjustments across expenditure categories.
- Compare budget execution between Q1 and Q2 of 2026.
- Highlight key financial insights through an executive dashboard.

## Tools & Technologies

- **Power BI** — Dashboard development and data visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — KPI calculations and financial measures

## Data Source

- **Publishing entity:** Ministry of Environment, Water and Agriculture (MEWA), Saudi Arabia
- **Data source:** [Saudi National Open Data Platform](https://open.data.gov.sa/)
- **Reporting periods:** Q1 and Q2, 2026
- **Currency:** Saudi Riyal (SAR)

*The specific dataset link and applicable reuse license should be verified before redistributing the original data.*

## Data Preparation

Data preparation included:

- Reviewed the source data and column structure to understand the dataset.
- Removed irrelevant and empty records/columns, standardized data types, and performed data quality checks to prepare the dataset for analysis.
- Added `Quarter` and `Report Date` fields to identify the reporting period
- Appending Q1 and Q2 data into a consolidated table named `Budget_Fact` after checking the data structure.

### Data Model

The dashboard uses a **single-table analytical model** named `Budget_Fact`, containing data for both reporting periods.

The table includes budget allocations, spending, execution rates, expenditure categories, quarter identifiers, and reporting dates.

### Financial Calculation Approach

Budget and spending figures are treated as **cumulative reporting snapshots** rather than independent quarterly values.

To avoid double-counting, the dashboard uses the latest available reporting snapshot within the selected filter context. When all quarters are selected, the latest snapshot (Q2 2026) is used for the overall financial KPIs.

## Key Performance Indicators (KPIs)

1. Original Budget
2. Current Budget
3. Total Spent
4. Execution Rate
5. Remaining Budget
6. Budget Adjustment
7. QoQ Spending Growth

## Dashboard Features

### 1. Spent vs. Current Budget by Expense Type
Compares cumulative spending with the current budget allocation for each expenditure category.

### 2. Q1 vs. Q2 Execution Rate
Compares budget execution rates across the two reporting periods.

### 3. Budget Adjustment by Expense Type
Highlights budget increases and decreases across expenditure categories.

### 4. Expense Type Financial Summary
Provides a detailed breakdown of current budget, cumulative spending, execution rate, remaining budget, and budget adjustments.

### 5. Executive Key Insights
Summarizes notable spending patterns, high execution rates, and significant budget adjustments.

## Key Findings

Based on the Q2 2026 reporting snapshot:

| KPI | Result |
|---|---:|
| Current Budget | SAR 12.93 billion |
| Cumulative Spending | SAR 8.29 billion |
| Execution Rate | 64.09% |
| Remaining Budget | SAR 4.64 billion |
| Budget Adjustment | +SAR 351.65 million |
| QoQ Spending Growth | Approximately 67% |

Additional observations:

- **Goods & Services** recorded the highest cumulative spending, at approximately SAR 4.56 billion.
- **Other Expenses** had the highest budget execution rate, at approximately 79%.
- **Other Expenses** also recorded the largest positive budget adjustment, at approximately SAR 333.13 million.

These findings describe the analyzed data and do not represent official assessments or recommendations issued by MEWA.

## Project Scope & Limitations

- The analysis covers Q1 and Q2 of 2026.
- Spending values represent cumulative reporting-period figures, not standalone quarterly expenditure.
- The model uses a single analytical table.
- The dashboard focuses on descriptive financial analysis and does not include forecasting.
- Results depend on the completeness and accuracy of the published source data.

## Dashboard Preview

Add your dashboard screenshot to the `images` folder and name it `dashboard.png`.

Then uncomment the following line:

<!-- ![MEWA 2026 Budget Performance Dashboard](images/dashboard.png) -->

## Disclaimer

This is an independent data analytics portfolio project developed using publicly available government data. It is **not an official MEWA dashboard** and is not endorsed by the Ministry of Environment, Water and Agriculture.

