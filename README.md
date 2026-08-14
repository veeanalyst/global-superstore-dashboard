# Global Superstore — Executive Sales & Profitability Dashboard

**AnalystLab Africa — Week 2 Data Analytics Project (Business Intelligence & Interactive Dashboard Development)**

## Business Problem

AnalystLab Africa Consulting was engaged by a national retail company to design an executive dashboard enabling management to monitor sales performance, profitability, customer behavior, and regional performance — using the [Global Superstore dataset](https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset) (51,290 order line items, 2011–2014, 7 global markets).

## Key Findings

| Driver | Finding |
|---|---|
| **Technology** | Top category by both volume (8K orders, $4.74M sales) and margin (13.99% vs. 11.61% baseline) |
| **Tables** | Unprofitable company-wide — a $64,083 loss and -8.46% margin, dragging down every region/segment it touches |
| **Central** | Top region by sales ($2.82M) but below-average margin (11.03%), partly explained by Tables losses |
| **Home Office** | Smallest segment (18.3% of sales) but above-average efficiency (11.99% margin) |
| **Canada** | Highest regional margin (26.62%) but on a small sample (201 orders) — flagged for testing, not treated as proven |
| **Seasonality** | Consistent November–December sales peak in 3 of 4 years, on top of steady year-over-year growth |

Overall company baseline: **$12.64M total sales, $1.47M profit, 25,035 orders, 11.61% profit margin.**

## Repository Structure

```
├── data/         Raw dataset (CSV)
├── reports/      BI Overview Report, Dataset Inspection Report, Executive Summary Report (Word)
└── dashboard/    Power BI project file (.pbix) and dashboard export
```

## Methodology

1. **Data preparation** — imported via Power Query; investigated and resolved a Postal Code completeness issue (80.5% missing, excluded from analysis), converted Order Date/Ship Date from text to proper dates (required an explicit UK locale setting to parse DD-MM-YYYY correctly), and verified 38 apparent duplicate Order+Product pairs as legitimate separate line items.
2. **Dashboard development** — built 5 KPI measures in DAX (Total Sales, Total Profit, Total Orders, Average Sales, Profit Margin), 8 visualizations spanning bar, column, line, donut, map, and matrix types, and 3 interactive slicers (Region, Category, Date).
3. **Insight synthesis** — used the dashboard's interactivity itself (clicking through regions, segments, and categories) to surface insights, cross-checking every claim against the underlying numbers before writing it up.
4. **Recommendations** — five actionable recommendations, each paired with a concrete next step rather than a vague direction to "investigate further."

## Recommendations Summary

1. Cap/reduce discounts on the Tables sub-category company-wide, alongside a full cost review.
2. Apply the same discount fix to Central's Tables sub-category as a fast win.
3. Run a small pilot marketing campaign in Canada to test whether its high margin holds at scale.
4. Reallocate marketing/inventory investment toward Technology.
5. Increase inventory and launch marketing ahead of the confirmed November–December peak.

## Tools Used

Microsoft Power BI (Power Query, DAX, interactive dashboards), Microsoft Word (written reports).

## Author

*Veronica Gika* — AnalystLab Africa Internship, Week 2
