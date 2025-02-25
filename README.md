# Online Retail Project




## Problem Statement

This dashboard helps the Chief Marketing Officer (CMO) and the management team of a global retail company to gain deep insights into their stock sales data across different countries. It enables them to understand sales performance, identify top-performing products, evaluate market share, and uncover opportunities for growth in various regions. By analyzing these insights, the company can make data-driven decisions to optimize sales strategies, enhance market presence, and improve overall profitability.

## Steps Followed
### Data Preparation and Loading
 1) Load Data: Load sales data into Power BI Desktop from a CSV file.
 2) Open Power Query Editor: In the View tab under the Data Preview section, check "Column Distribution," "Column Quality," and "Column Profile" options.
 3) Ensure Column Profiling: Ensure column profiling is based on the entire dataset.
### Data Cleaning and Transformation
 1) Error and Empty Value Handling: Observe any errors and empty values in the columns. For instance, if the "Stock Quantity" column has missing values, handle them appropriately.
 2) Exclude Null Values: For calculating average sales, exclude null values from consideration as they may not significantly impact the results.

#### DAX code
Product Group = 

FilteredQuantity = IF('Online Retail'[Quantity] >= 1, 'Online Retail'[Quantity], BLANK())

FilteredUnitPrice = IF('Online Retail'[UnitPrice] >= 0 , 'Online Retail'[UnitPrice], BLANK())

 5) Create Measures for Key Metrics: Create measures for key metrics such as the total Revenue.
#### DAX code
Revenue = 'Online Retail'[FilteredQuantity] * 'Online Retail'[FilteredUnitPrice]

 

### Publishing and Insights
 1) Publish to Power BI Service: Publish the report to Power BI Service.

### Insights
A single-page report was created on Power BI Desktop and then published to Power BI Service. The following insights can be drawn from the dashboard:

#### General Sales Performance
- Monthly Sales Trends: Shown in a line chart, illustrating the sales trends over Monthly.

Monthly Revenue visual
![Monthely Revenue](https://github.com/user-attachments/assets/37854878-5230-4dc3-9920-76e353616ef8)

#### Customer Segmentation by each Cointry
- Customer Segmentation: Displayed in a clustered column chart, showing the distribution of customer segments in each country.

Snap Of Each Country Revenue
![Revenue by country](https://github.com/user-attachments/assets/98d2fdb2-3ab4-4d4a-93b8-bbccb3ed59f3)

####  Top 10 Customers by Revenue
-  Created a visual for the revenue generated by the top 10 customers in a column chart, providing a clear comparison of their contributions to the overall revenue.

Snap of Top 10 Customers Revenue
![Top 10 Customers Revenue](https://github.com/user-attachments/assets/75bd2ce0-c5e4-47b6-bbef-d9abd711c153)
#### Stock Demand by Country
- Displayed a visual showing the demand for stocks in various countries using a map chart in Power BI, providing a geographic perspective on stock demand distribution.

Snap of Stock Demand by Country
![Stocks Demand By Country](https://github.com/user-attachments/assets/f5e9cd9d-01ba-4cb8-ba4b-692d6f682277)

### Conclusion
This dashboard provides the CMO and the management team with comprehensive insights into stock sales data across different countries, enabling them to make informed strategic decisions to optimize sales performance, enhance customer satisfaction, and improve overall profitability.
