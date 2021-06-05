# Sales-Insights-Data-Analysis
Used MySQL and Tableau to conduct conduct data analysis of sales (profit &amp; revenue) and represent the findings via interactive dashboards 

## Technologies used : 
1. MySQL 
2.  Tableau 

## Steps : 
1. Preliminary Data Exploration using SQL 
2.  Data Cleaning & ETL through Tableau 
3.  Data Analysis of revenue and profit using Tableau
4.  Creating interactive dashboard using Tableau

### Preliminary Data Exploration using SQL
1. Show all customer records

2. SELECT * FROM customers;

3. Show total number of customers

4. SELECT count(*) FROM customers;

5. Show transactions for Chennai market (market code for chennai is Mark001

6. SELECT * FROM transactions where market_code='Mark001';

7. Show distrinct product codes that were sold in chennai

8. SELECT distinct product_code FROM transactions where market_code='Mark001';

9. Show transactions where currency is US dollars

10. SELECT * from transactions where currency="USD"

11. Show transactions in 2020 join by date table

12. SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

13. Show total revenue in year 2020,

14. SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and    transactions.currency="INR\r" or transactions.currency="USD\r";

15. Show total revenue in year 2020, January Month,

16. SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

17. Show total revenue in year 2020 in Chennai

18. SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
