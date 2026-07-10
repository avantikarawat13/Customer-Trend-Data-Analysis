# Customer Shopping Behavior Analysis

Analysis of 3,900 retail transactions to uncover customer spending patterns, segments, and subscription behavior — using Python, SQL, and Power BI.

## Problem

The raw transactional dataset held unexamined patterns in spending, subscriptions, and discount usage, with no clear view into which customer segments, product categories, or shipping strategies were actually driving revenue.

## Solution

- **Data Cleaning (Python / pandas):** Loaded and explored the dataset, imputed 37 missing `review_rating` values using category-level medians, standardized column names to snake_case, and removed the redundant `promo_code_used` column.
- **Feature Engineering:** Created `age_group` (via age binning) and `purchase_frequency_days` to support segmentation analysis.
- **SQL Analysis (PostgreSQL):** Loaded the cleaned data into PostgreSQL and wrote 10+ queries to answer business questions — revenue by gender, high-spending discount users, top-rated products, shipping type comparison, subscriber vs. non-subscriber spend, discount-dependent products, customer segmentation, top products per category, repeat buyer/subscription correlation, and revenue by age group.
- **Dashboard (Power BI):** Built an interactive dashboard with filters for subscription status, gender, category, and shipping type to visualize revenue and sales trends.

## Result

- Non-subscribers generated **$170K** in total revenue vs. **$63K** from subscribers.
- **5 products** (Hat, Sneakers, Coat, Sweater, Pants) relied on discounts for **47–50%** of their sales.
- **80%** of customers (3,116 of 3,900) fell into the "Loyal" segment, based on purchase history.
- Findings informed recommendations on subscription incentives, loyalty programs, discount policy, and targeted marketing toward high-revenue age groups and express-shipping users.

## Dataset

| | |
|---|---|
| Rows | 3,900 |
| Columns | 18 |
| Key features | Age, Gender, Location, Subscription Status, Item Purchased, Category, Purchase Amount, Season, Size, Color, Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type |

## Tech Stack

- **Python** (pandas) — data cleaning, exploration, feature engineering
- **PostgreSQL** — structured business-question analysis via SQL
- **Power BI** — interactive dashboard for visual reporting

## Dashboard Preview

The Power BI dashboard includes KPI cards (customer count, average purchase amount, average review rating), a subscription status breakdown, and revenue/sales charts by category and age group, all filterable by gender, category, shipping type, and subscription status.

## Repository Structure

```
├── data/               # Raw and cleaned datasets
├── notebooks/          # Python data cleaning & EDA scripts
├── sql/                # SQL queries for business analysis
├── dashboard/          # Power BI dashboard file
└── README.md
```

## Business Recommendations

- **Boost Subscriptions** — Promote exclusive benefits for subscribers.
- **Customer Loyalty Programs** — Reward repeat buyers to move them into the "Loyal" segment.
- **Review Discount Policy** — Balance sales boosts with margin control.
- **Product Positioning** — Highlight top-rated and best-selling products in campaigns.
- **Targeted Marketing** — Focus efforts on high-revenue age groups and express-shipping users.
