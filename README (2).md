# Superstore Executive Dashboard

An interactive, single-file HTML dashboard built for executive-level reporting on US retail transactions (2018–2021). Open `index.html` in any modern browser. No build step or server is required.

**Live demo:** `https://harsh088c-debug.github.io/retail-profitability-dashboard/](https://harsh088c-debug.github.io/retail-profitability-dashboard/superstore_dashboard.html`

## Features

- **5 KPI cards:** Revenue, Profit, Profit Margin, Orders, Unique Customers, each with a year-over-year trend indicator
- **Global filters** that drive every chart at once: Year, Region, Segment, Category, Ship Mode
- **11 interactive charts:**
  1. Monthly sales and profit trend (dual axis)
  2. Sales by category (donut)
  3. Profit margin by sub-category (colour-coded: green above 15%, amber 0–15%, red negative)
  4. Regional sales with profit margin line
  5. Segment revenue by year (stacked)
  6. Sales vs profit bubble chart (bubble size = quantity)
  7. Discount impact on average profit
  8. Top 10 states by revenue (coloured by region, margin label)
  9. Ship mode distribution with days-to-ship and profit table
  10. Year-over-year sales and profit with growth labels
  11. Orders heatmap (month × day of month)
- **5 automated insights** that rewrite themselves when filters change
- Tooltips on every chart, 200 ms transitions, light and dark theme support

## Tech

- All 9,994 rows are embedded in the file, with no API calls

## Data

Source: `SuperStore_Data.xlsx` (sheet `Orders`), 9,994 line items across 5,009 unique orders and 793 customers.

### Known data-quality issues

- **Placeholder sales values:** 11 line items (the first 11 rows) have an identical Sales value of exactly $50,000 while their profit values look normal. They add about $550K to total revenue. The dashboard includes them by default so totals match the raw file ($2.84M revenue, 10.1% margin). Tick the checkbox at the top of the dashboard to exclude them (about $2.29M revenue, 12.5% margin).
- **"Orders" vs line items:** the file has 9,994 rows, but only 5,009 unique order IDs. The Total Orders card shows unique orders; the line-item count appears on hover.

## Deploy with GitHub Pages
1. Go to **Settings → Pages**, choose **Branch: main / root**, then Save.
2. The site goes live within a few minutes.

## Note

This repository does not include the raw Excel file. The embedded data holds only numeric values and category codes, with no customer names.
