# VEDA TECHNOLOGY — Task 26 Power BI Build Guide

## 1. Import data
1. Open Power BI Desktop.
2. Select **Get Data → Text/CSV**.
3. Choose `Superstore_Cleaned_Dashboard_Data.csv`.
4. Select **Transform Data** if you need to verify types.
5. Confirm `Order.Date` and `Ship.Date` are Date fields.
6. Load the data.

## 2. Rename the table
Rename the imported table to:

`Superstore`

## 3. Create the Date table
Open **Modeling → New Table** and paste the Date table from `PowerBI_DAX_Measures.txt`.

Then:
- Select the Date table.
- Choose **Table tools → Mark as date table**.
- Select `Date[Date]`.

## 4. Create the relationship
In Model view create:

`Date[Date]` → `Superstore[Order.Date]`

Use a one-to-many relationship with Date on the one side.

## 5. Add measures
Copy the KPI measures from `PowerBI_DAX_Measures.txt` into the Superstore model.

Recommended first six cards:
- Total Sales
- Total Profit
- Profit Margin
- Orders
- Customers
- Average Order Value

## 6. Apply the theme
Open **View → Themes → Browse for themes** and select:

`VEDA_Executive_Dashboard_Theme.json`

## 7. Build the one-page layout
### Header
VEDA TECHNOLOGY | EXECUTIVE KPI DASHBOARD

### Slicers
- Year
- Region
- Category
- Segment
- Ship Mode
- Order Priority

### KPI cards
- Total Sales
- Total Profit
- Profit Margin
- Orders
- Customers
- Average Order Value

### Charts
1. Line/column chart — Sales and Profit by Year-Month.
2. Bar chart — Sales by Region.
3. Bar chart — Top 10 Sub-Categories by Sales.
4. Table — Sales, Profit, Margin and Orders.
5. Watchlist — lowest-profit sub-categories.

## 8. Formatting
- Sales / Profit: `$#,##0`
- Margin: `0.0%`
- Counts: `#,##0`
- Keep the page clean and aligned.
- Avoid more than 6–8 major visuals.
- Use tooltips for secondary detail.

## 9. Validation
The dashboard should approximately reconcile to:
- Sales: $12.64M
- Profit: $1.47M
- Margin: 11.6%
- Orders: 25,035
- Customers: 4,873

## 10. Publish
1. Save as `VEDA_Task_26_Executive_KPI_Dashboard.pbix`.
2. Publish to the required Power BI workspace.
3. Test filters after publishing.
4. Copy the report/repository links required by the internship portal.
