# Superstore Sales Analysis

**Prepared by:** Joseph Amare  
**Dataset:** [Superstore Dataset (Kaggle)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

## Project Overview

This project explores retail orders, sales, discounts, and profit in the Superstore dataset. The goal is to identify business patterns, areas of strong and weak performance, and opportunities to improve profitability and service.

The dataset is commonly distributed as `Sample - Superstore.csv`. Column names and date formats can vary between copies, so inspect the downloaded file before starting analysis.

## Analysis Objectives

- Measure overall sales, profit, order volume, and average order value.
- Find how sales and profit change over time, including seasonal patterns.
- Compare results across regions, states, cities, customer segments, and ship modes.
- Identify the strongest and weakest product categories and sub-categories.
- Examine how discounting relates to sales and profit.
- Identify high-value customers and products with high sales but low or negative profit.
- Review shipping patterns and delivery times where the available dates allow.
- Provide clear, evidence-based business recommendations.

## Possible Analysis Tasks

### 1. Data Inspection and Preparation

- Check row counts, column names, data types, missing values, duplicates, and invalid values.
- Parse `Order Date` and `Ship Date` as dates.
- Check whether `Postal Code` contains missing values.
- Confirm that `Sales`, `Profit`, and `Discount` are numeric and `Quantity` contains sensible values.
- Review unusual values, such as negative profit, extreme discounts, or zero or negative sales.
- Confirm the unit of analysis. A row is typically an order line, so an order may appear in multiple rows.

### 2. Business Performance

- Calculate total sales, total profit, total quantity, distinct orders, and distinct customers.
- Calculate profit margin as total profit divided by total sales.
- Calculate average order value.
- Compare monthly and yearly sales and profit.
- Compare performance by region, state, city, customer segment, category, and sub-category.
- Rank products and groups by sales, profit, and profit margin.

### 3. Discounts and Profitability

- Compare profit and profit margin across discount levels.
- Find products, locations, or customer groups with high sales but low or negative profit.
- Check whether higher quantities or sales offset the margin impact of discounts.
- Avoid treating a relationship between discount and profit as proof of cause and effect.

### 4. Customer Analysis

- Rank customers by sales and profit.
- Compare customer rankings by sales with rankings by profit.
- Analyze order frequency, average order value, and recency if dates are available.
- Explore product preferences and profitability by customer segment.
- Document the definitions and time period used for customer segmentation.

### 5. Shipping Analysis

- Compare orders, sales, and profit by `Ship Mode`.
- Calculate shipping duration as `Ship Date - Order Date`.
- Check for negative or implausible shipping durations.
- Avoid conclusions about promised delivery times or shipping costs if those fields are unavailable.

### 6. Visualizations and Recommendations

- Create time-series charts for sales and profit.
- Use ranked bar charts for regional and product comparisons.
- Show both sales and profit or margin, rather than revenue alone.
- Support each recommendation with a metric, affected group, and any relevant assumptions.

## Dataset Fields

| Field | Description |
|---|---|
| `Row ID` | Identifier for a dataset row |
| `Order ID` | Order identifier; may repeat across line items |
| `Order Date` | Date the order was placed |
| `Ship Date` | Date the order was shipped |
| `Ship Mode` | Shipping service or mode |
| `Customer ID` | Customer identifier |
| `Customer Name` | Customer name |
| `Segment` | Customer segment |
| `Country` | Country associated with the order |
| `City` | City associated with the order |
| `State` | State associated with the order |
| `Postal Code` | Postal code; may contain missing values |
| `Region` | Sales region |
| `Product ID` | Product identifier |
| `Category` | Broad product category |
| `Sub-Category` | Product sub-category |
| `Product Name` | Product name |
| `Sales` | Sales amount for the order line |
| `Quantity` | Units on the order line |
| `Discount` | Discount recorded for the line |
| `Profit` | Profit recorded for the line |

## Suggested Key Metrics

- **Total Sales:** Sum of `Sales`.
- **Total Profit:** Sum of `Profit`.
- **Profit Margin:** Total Profit divided by Total Sales.
- **Order Count:** Distinct count of `Order ID`, not the number of rows.
- **Average Order Value:** Total Sales divided by distinct Order Count.
- **Units Sold:** Sum of `Quantity`.
- **Average Shipping Duration:** Average days between `Order Date` and `Ship Date`, after validating dates.

## Suggested Workflow

1. Download the dataset from Kaggle and record its version or download date.
2. Inspect and clean the data, documenting exclusions and transformations.
3. Define metrics and the unit of analysis before aggregating.
4. Explore overall trends, then compare segments and products.
5. Validate notable findings against the underlying rows.
6. Present key findings, charts, recommendations, and limitations.

## Important Considerations

- The dataset contains historical transactions and may not reflect current products, prices, or operations.
- `Sales` and `Profit` are order-line measures; aggregate them carefully to avoid double-counting orders.
- The dataset may not include costs, inventory, returns, delivery promises, or customer demographics.
- Correlation between discount and profit does not prove that discounts caused lower profit.
- Consider group size and outliers, and state the time period behind each comparison.

## Tools

The dataset can be analyzed with Python (pandas, matplotlib, seaborn), R, SQL, Excel, Tableau, or Power BI.
