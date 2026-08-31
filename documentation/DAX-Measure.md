</> Markdown
# DAX Calculations
This document describes the calculated columns and measures developed for the Sales Performance Dashboard.
## Calculated Columns

### 1. Year
```DAX
Year = YEAR([Date])
Extracts the year from the Date field to support time-based analysis and filtering.

2. Profit Margin
 </> DAX 
 Profit Margin = DIVIDE([Sales] - [Cost], [Sales]) * 100
 Calculates the profit margin for each record based on sales and cost

 Measures
 
 1. Average Profit Margin 
 </> DAX
 Average Profit Margin = AVERAGE('Sales Performance Data'[Profit Margin])
 Calculates the average profit margin across the selected records
 
 2. Total Profit 
 </> DAX 
 Total Profit = SUMX('Sales Performance Data', 'Sales Performance Data'[Sales] - 'Sales Performance Data'[Cost])
 Calculates total profit by subtracting cost from sales for each record and aggregating the results

 Skills Demonstrated 
 * Dax calculated columns 
 * DAX measures
 * Aggregating using AVERAGE
 * Row-level calculations using SUMX
 * Profitability analysis
 * Time-based analysis
