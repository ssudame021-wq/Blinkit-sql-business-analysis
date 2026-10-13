# Blinkit-sql-business-analysis
20 SQL queries on 36.8 lakh Blinkit quick-commerce orders (2022-2026): revenue growth, customer tiers, store performance, delivery speed, promo codes and retention. MySQL, CTEs, window functions.
# Blinkit SQL Business Analysis

**What drives a quick-commerce business: growth, loyal customers, fast delivery, or discounts? I used 20 SQL queries on 36.8 lakh orders to find out.**

## Project overview

This project analyses Blinkit-style quick-commerce order data from 2022 to 2026. Each of the 20 queries starts with a plain business question, answers it in MySQL, and ends with a recommended action. The full walkthrough is in the slide deck.

- **Data:** 36.8 lakh delivered orders, 7.41 lakh customers, ₹375 Cr revenue
- **Tools:** MySQL, MySQL Workbench
- **SQL skills:** CTEs, window functions (LAG, RANK, NTILE), CASE segmentation, cohort analysis

## What I found

1. **The business is growing.** Revenue went from ₹30.9 Cr in 2022 to ₹151 Cr in 2025, and average order value rose every year (₹739 to ₹1,256). 2026 is a partial year.
2. **Repeat customers are the business.** They bring ₹367 Cr of the ₹375 Cr total, so retention matters more than acquisition.
3. **Loyalty tiers lift basket size, not frequency.** Reorder rate is almost flat, from 63.7% (Bronze) to 65.1% (Platinum).
4. **Speed pays off.** Express orders arrive in 10.7 min against 30.8 min, and customers rate them slightly higher (4.37 vs 4.33).
5. **Not all promo codes are equal.** UPIOFF drives 12.9% of revenue at a much lower discount cost than SAVE20 or FESTIVE25.

## Business questions covered

| Theme | Questions |
|-------|-----------|
| Growth | Overall KPIs, year-over-year growth, monthly trends |
| Stores | Top stores, ranking within each city, failure rates, slow high-volume stores, operational risk score |
| Customers | High-value customers, tier performance, reorder rate, first-time vs repeat revenue |
| Delivery | Delivery slots vs ratings, express eligibility vs delivery time |
| Promotions | Promo vs no promo, promo codes ranked by revenue |
| Retention | Cohort retention, customers at risk of churn, revenue concentration |

## Repository structure

- `data/`: order data (yearly CSV files)
- `sql/`: table setup and the 20 analysis queries
- `outputs/`: query results from MySQL Workbench
- `presentation/`: slide deck with problem, query, output and solution for each question

## How to run

1. Create the table with the setup script in `sql/` (the table is named `blinkit`).
2. Load the yearly CSV files into it.
3. Run the queries one by one and compare with the screenshots in `outputs/`.

Full CSV files: [add Google Drive link]

## Notes

- Query 17 shows a `0000-00` cohort because some order dates loaded as `0000-00-00`. Clean or filter those before charting retention.
- This is a dataset-based portfolio project, not official Blinkit data.

## Author

[Your name] | [LinkedIn link]
