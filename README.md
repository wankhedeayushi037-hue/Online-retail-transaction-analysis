
# Online Retail Transaction Analysis

## Project Overview

This project explores online retail transaction data using Python to understand sales trends, product performance, customer purchasing behaviour, and country-level performance.

The analysis focuses on data quality, transaction values, cancellations, and business insights derived from historical retail records.

## Business Objectives

- Identify monthly sales trends.
- Analyse product performance by transaction value.
- Compare sales across countries.
- Identify customers with the highest net transaction value.
- Examine weekday sales patterns.
- Investigate missing values, duplicate records, and potential cancellations.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset

**Source:** UCI Machine Learning Repository — Online Retail Dataset

https://archive.ics.uci.edu/dataset/352/online+retail

The dataset contains transaction records with invoice numbers, product codes, descriptions, quantities, invoice dates, unit prices, customer IDs, and countries.

## Project Workflow

1. Loaded and inspected the retail dataset.
2. Audited missing values, duplicate rows, and unusual quantities and prices.
3. Investigated cancellation invoices and negative quantities.
4. Calculated line-level transaction value using Quantity × UnitPrice.
5. Removed exact duplicate records from the working dataset.
6. Analysed monthly, product-level, country-level, and customer-level transaction values.
7. Examined invoice counts and weekday trends.
8. Created charts to communicate key findings.

## Data Quality Findings

- Original dataset: 541,909 rows.
- Exact duplicate rows identified: 5,268.
- Working dataset after removing exact duplicates: 536,641 rows.
- CustomerID was missing in approximately 25% of the original records.
- Negative quantities and zero or negative unit prices were investigated as potential data-quality or return-related issues.

## Key Business Insights

- **Monthly trend:** November 2011 recorded the highest monthly net line value.
- **Country performance:** The United Kingdom had the highest net line value.
- **Product analysis:** DOTCOM POSTAGE ranked highest by net line value, but it represents a service charge rather than a merchandise product.
- **Customer analysis:** Customer 14646 had the highest net line value among customers with known IDs.
- **Weekday analysis:** Thursday recorded the highest net line value among weekdays.
- **Invoice analysis:** The dataset contained 25,900 unique invoice numbers, including 3,836 invoice numbers beginning with "C".

## Important Limitations

- Net line value is calculated as Quantity × UnitPrice; it should not be interpreted as verified revenue or profit.
- Invoice numbers beginning with "C" were treated as cancellation indicators for investigation, but cancellation and return business rules require further validation.
- Customer-level analysis excludes records with missing CustomerID.
- December 2011 is incomplete because the dataset ends on 9 December 2011.
- The dataset does not include an explicit currency column; pound sterling is inferred from the UK retail context.

## Conclusion

This project demonstrates practical Python skills in data auditing, cleaning, exploratory data analysis, grouping, aggregation, and visualisation. The analysis shows how retail transaction data can be used to explore sales patterns, customer activity, and product and market performance.
