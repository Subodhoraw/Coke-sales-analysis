# Coke Sales Analysis with Microsoft Excel

An Excel-based retail sales analysis project exploring revenue, unit volume, retailer performance, regional distribution, beverage-brand contribution, monthly trends, and operating profitability across U.S. retailers.

> **Project status:** Workbook inspection and initial data-quality review completed. The portfolio-ready interactive dashboard, final insight validation, and recorded presentation are planned next steps—not claimed as completed deliverables.

## Business question

How can Coca-Cola optimise sales performance and operating profitability across U.S. retailers, regions, beverage brands, and time periods?

## Dataset overview

The supplied workbook contains a main transaction sheet with **3,888 records** and **13 fields**, covering **January–December 2021**. The data represents four retailers, six beverage brands, and five U.S. sales regions.

### Fields

- Retailer and Retailer ID
- Invoice Date
- Region, State, and City
- Beverage Brand
- Price per Unit and Units Sold
- Total Sales
- Operating Profit and Operating Margin
- Month

## Workbook contents

The original workbook is included in [`data/`](data/Coke-sales-analysis-solution.xlsx). Its worksheets are:

| Worksheet | Purpose |
|---|---|
| `Data` | Main transaction-level dataset |
| `Beginner` | Basic monthly and retailer sales analysis |
| `Intermediate` | Monthly sales and beverage-brand analysis |
| `Advanced` | Units sold by region and brand |
| `Addtional Analysis` | Additional analysis prompts |

## Initial baseline findings

These are preliminary calculations from the supplied workbook and should be revalidated in the final cleaned model and PivotTables.

| Metric | Initial result |
|---|---:|
| Total sales | 8,684,027.50 |
| Total operating profit | 3,173,631.88 |
| Total units sold | 17.15 million |
| Weighted operating margin | 36.55% |
| Highest-sales retailer | Sodapop — 4,403,630 |
| Highest-sales region | West — 2,835,100 |
| Highest-sales beverage brand | Coca-Cola — 2,015,890 |
| Highest-sales month | December — 1,045,775 |
| Lowest-sales month | March — 483,530 |

**Metric note:** Weighted operating margin is calculated as total operating profit divided by total sales. It is not the simple average of row-level margins. The workbook does not explicitly specify the currency, so values are presented without a currency symbol.

## Initial data-quality review

The first review identified:

- No blank cells in the inspected transaction fields.
- No exact duplicate transaction rows.
- No negative units or sales values.
- No mismatches in the checked `Price per Unit × Units Sold` sales calculation.
- Two records with zero units and zero sales but a recorded operating margin of 40%. These records are flagged for investigation rather than silently removed.

## Analysis workflow

1. Preserve the supplied workbook as the raw source.
2. Create a clean, structured Excel Table for the transaction data.
3. Validate column types, dates, numeric measures, and exceptional records.
4. Use formulas and/or Power Query for repeatable preparation.
5. Build PivotTables for retailer, region, state, brand, and month analysis.
6. Compare revenue, units sold, operating profit, and weighted operating margin.
7. Build an interactive dashboard with PivotCharts, slicers, and date filtering.
8. Document validated findings and evidence-based recommendations.
9. Record a short walkthrough explaining the business question, preparation, analysis, dashboard, and recommendations.

## Planned dashboard components

- KPI cards: Total Sales, Units Sold, Operating Profit, Weighted Operating Margin
- Sales by retailer
- Sales by region and state
- Sales by beverage brand
- Monthly sales trend
- Operating profit and margin comparisons
- Slicers for retailer, region, state, and beverage brand; date filtering where supported

## Tools and Excel skills

- Microsoft Excel Tables and structured references
- Data validation and data-quality checks
- SUMIFS, COUNTIFS, IF, IFERROR/IFNA, and date functions where appropriate
- PivotTables and PivotCharts
- Conditional formatting and heatmap-style views
- Slicers and interactive filtering
- Power Query for repeatable data preparation (planned)

## Repository structure

```text
coca-cola-sales-analysis/
├── README.md
├── .gitignore
├── data/
│   └── Coke-sales-analysis-solution.xlsx
└── docs/
    ├── analysis-plan.md
    ├── data-dictionary.md
    └── presentation-outline.md
```

## Data use and attribution

The workbook was supplied for this project. Its external source and redistribution licence were not included with the file. Before making this repository public, verify that you have permission to redistribute the dataset. If redistribution is not permitted, publish the analysis documentation and a small synthetic sample instead, and keep the original workbook private.

## Reproducibility

All headline results in this README are preliminary. The final version should show the exact PivotTable or formula logic used to reproduce each KPI and should document any treatment of exceptional records.

