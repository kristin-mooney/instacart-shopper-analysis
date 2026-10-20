# Instacart Shopper Behavior Analysis

[![Tableau Public](https://img.shields.io/badge/Tableau-Public-blue?logo=tableau)](https://public.tableau.com/app/profile/kristin.mooney/viz/InstacartAnalyticsProject/UnderstandingInstacartShopperBehavior)
[![dbt](https://img.shields.io/badge/dbt-Transformation-green?logo=dbt)](https://kristin-mooney.github.io/instacart-analytics/)

A three-dashboard Tableau story answering three specific business questions using the Kaggle Instacart dataset: *when* do customers shop, *what* drives reorder behavior, and *who* are the most valuable customers? Built using dbt to transform 3.4 million grocery orders into analysis-ready mart models, then connected to Tableau for visualization — structured as a full end-to-end analytics workflow.

---

## [View the Live Dashboard on Tableau Public](https://public.tableau.com/app/profile/kristin.mooney/viz/InstacartAnalyticsProject/UnderstandingInstacartShopperBehavior)

---

## Dashboard Overview

### Dashboard 1 — When Customers Shop
![When Customers Shop](<screenshots/When Customers Shop.png>)

Analyzes order volume by day of week and hour of day. Includes:
- **Order Volume Heatmap** — day × hour grid showing peak demand windows
- **Orders by Day of Week** — Saturday leads at 600,905 orders; Saturday + Sunday = 35% of weekly volume
- **Hourly Order Trend** — negligible overnight activity, rapid surge from 7–10am, peak at 284,728 orders at 10am

---

### Dashboard 2 — What Customers Are Buying
![What Customers Are Buying](<screenshots/What Customers are Buying.png>)

Analyzes product department performance by volume and reorder loyalty. Includes:
- **Reorder Rate by Department** — Dairy & Eggs leads at 51%, Pets at 49%; Personal Care lowest at 23%
- **Total Orders by Department** — Produce dominates at 9.4M orders (29% of all orders)
- **Top Products Scatter Plot** — Organic Whole Milk, Banana, and Organic Strawberries lead on both volume and reorder rate

---

### Dashboard 3 — Shopper Loyalty Segments
![Shopper Loyalty Segments](<screenshots/Shopper Loyalty.png>)

Segments 200,000+ customers by order frequency and shopping cadence. Includes:
- **Customer Distribution** — At-Risk (30%), Regulars (29%), New & Active (23%), Loyalists (19%)
- **Order Contribution** — Loyalists (19% of customers) drive 41% of total orders; At-Risk (30%) contribute just 12%
- **Days Between Orders** — Loyalists shop every 6 days; At-Risk every 24 days

---

## Key Findings

| Insight | Detail |
|---|---|
| Weekend Concentration | Saturday & Sunday account for 35% of all weekly orders |
| Morning Peak | Orders peak at 10am (284,728 orders); overnight hours nearly inactive |
| Produce Dominates Volume | Produce = 29% of all orders — nearly 3× the next largest department |
| Dairy Anchors Loyalty | Dairy & Eggs reorder rate: 51% — highest of any department |
| Loyalists Drive Revenue | 19% of customers → 41% of total order volume |
| At-Risk Gap | At-Risk customers (30% of base) contribute only 12% of orders, shopping every 24 days |

---

## Tools Used

- **dbt** — staging → marts SQL transformation pipeline
- **SQL** — data modeling and aggregation
- **Tableau Desktop & Tableau Public** — three-dashboard story and publishing

---

## Data Source

- **Kaggle Instacart Online Grocery Shopping Dataset (2017)** — ~3.4 million grocery orders from 200,000+ anonymized users across 50,000+ products

---

## Repository Structure

```
├── screenshots/
│   ├── dashboard1-when-customers-shop.png
│   ├── dashboard2-what-customers-buy.png
│   └── dashboard3-loyalty-segments.png
├── dbt/
│   ├── mart_timing_analysis.sql
│   ├── mart_product_performance.sql
│   └── mart_user_rfm.sql
└── README.md
```

---

*Built by [Kristin Mooney](https://kristin-mooney.github.io/) | [LinkedIn](https://linkedin.com/in/kristinmooney) | [Portfolio](https://kristin-mooney.github.io/instacart-analytics/)*
