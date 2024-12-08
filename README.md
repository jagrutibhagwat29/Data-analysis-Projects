# Sales Analysis for a Food Trade Company
XYZ company deals with sales amongst 8 different categories food. This sales analysis relates in examining various aspects of the company's sales performance to identify trends, strengths, weaknesses, and opportunities for improvement. 

## Datasets
OData feed- https://services.odata.org/Northwind/Northwind.svc/

## Here are the general steps for performing data analysis in Power BI:
•	Collect Data: Gather the necessary data from various sources such as Excel, databases, or cloud storage. Import this data into Power BI Desktop.
•	Clean the Data: Prepare your data for analysis by handling missing values, removing duplicates, and correcting errors.

•	Analyse the Data: Use Power BI's tools to explore and interpret your data. This can include creating visualizations, performing statistical analysis, and identifying trends and 
  patterns.

•	Communicate Results: Share your findings with others by creating reports, dashboards, and presentations within Power BI.

## Sales analysis dashboard includes
•	Total Sales- $504.17K

•	Quantity-19K

•	Total Sales by category, Total sales by country, Total sales by order date- Comparing the company's sales performance with that of competitors to identify areas where the company can 
  improve or differentiate itself

•	LY Sales, CY Sales, CY & LY comparison column chart- Assessing the performance of individual products or product lines to determine which items are the best sellers and which ones are 
  underperforming.

•	Top 10 customers visuals and top 5 product performance along with the detailed analysis of each food product as per year and country.

## DAX Expressions:
•	CY Sales (1998) = TOTALYTD([Total Sales], Date_Master[Date])

•	LY Sales (1997) = CALCULATE([CY Sales (1998)], SAMEPERIODLASTYEAR(Date_Master[Date]))

•	Sales of 1996 = CALCULATE([Total Sales], 'Fiscal year table'[Year] = YEAR(TODAY() - 1))

•	Total Sales = SUM(Order_Details[Sales]) + 0

•	Var. = [CY Sales (1998)] - [LY Sales (1997)]

•	YoY growth % = DIVIDE([Var.], [LY Sales (1997)], 0)

•	LastRefresh = "Report as of date: " & NOW()

## Technical insights:
•	Total Sales trended down, resulting in a 13.13% decrease between Monday, July 8, 1996 and Monday, April 13, 1998.  

•	Total Sales started trending down on Wednesday, March 25, 1998, falling by 23.86% ($493.50) in 19 days.  

•	 Total Sales dropped from $2,068.50 to $1,575.00 during its steepest decline between Wednesday, March 25, 1998 and Monday, April 13, 1998.  

•	 At $2,27,659.03, USA had the highest Total Sales and was 3,604.00% higher than UK, which had the lowest Total Sales at $6,146.30. 

•	Across all 6 Country, Total Sales ranged from $6,146.30 to $2,27,659.03. 

•	At 8236, Beverages had the highest LY Sales (1997) and was 1,485.07% higher than Seafood, which had the lowest LY Sales (1997) at 519.60. 

•	 LY Sales (1997) and total CY Sales (1998) are positively correlated with each other. 

•	 Across all 8 Category, LY Sales (1997) ranged from 519.60 to 8236, CY Sales (1998) ranged from 1,947.35 to 23197, and YoY growth % ranged from -61.00% to 1150.53%.  

•	At $72,515.20, Côte de Blaye had the highest Total Sales and was 221.68% higher than Tarte au sucre, which had the lowest Total Sales at $22,542.50.  

•	 Across all 5 ProductName, Total Sales ranged from $22,542.50 to $72,515.20. 


