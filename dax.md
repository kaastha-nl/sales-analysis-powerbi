# DAX Measures

**Average Order Value**
DAX
Copy code
Average Order Value =
DIVIDE ( SUM(Orders[TotalSales]), COUNT(Orders[OrderID]) )
sql
Copy code
**Month-over-Month Growth %**
DAX
Copy code
MoM Growth % =
DIVIDE (
    [Total Sales] - CALCULATE([Total Sales], DATEADD(Orders[OrderDate], -1, MONTH)),
    CALCULATE([Total Sales], DATEADD(Orders[OrderDate], -1, MONTH))
)
