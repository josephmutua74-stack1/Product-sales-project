## Product sales data
This is a data analysis project on sales from several region across the world, focusing on profits, gross revenue and customer reviews
I strived to draw insights and present the key KPis in an interactive excel dashboard

## key steps during the analysis phase
Check controls and Assumptions	
 Data Cleaning & Preparation:	 
 I went ahead to check for duplicates,identify missing values,correct data types,standardize text values,validate data values,check for outliers
   • Remove exact duplicate rows (define and document your duplicate criteria).	Here I used the Orderid column,with the assumption that this will be my primary key. Therefore I highlighted the the duplicated in conditional formatting and compared them then deleted. I only found 1 duplicate.
   • Fix data types (dates as Dates, numeric fields as numbers).	I formatted all my columns to their appropriate data types, Date for date columns,Text for text columns,Number for numeric columns.
   • Handle missing values for City, Salesperson, and Channel using reasonable business logic (document your approach).	There were several rows missing entries in the City column,Salesperson, and Channel. For the purposes of analysis, I autofilled unkwown,n/a and not assigned respectively.
   • Flag and correct suspicious UnitPrice values (e.g., negative prices) and discounts (e.g., > 30%).	I highlighted in bright yellow all the cells that had a negative value, the went ahead and used the absolute value function to correct them in a new column. I then went ahead and highlighted discounts that were above 30%
   • Ensure RequiredDate is not earlier than OrderDate; where it is, impute a corrected RequiredDate (explain your rule).	I used an IF function (if requireddate< orderdate) with a return value of valid and not valid since cannot logically precede the order being placed. I therefore set orderdate=requireddate to avoid 
ABC analysis on SKUs	In our case, we need to group SKUs within a product category based on their contribution to that category's total gross revenue

