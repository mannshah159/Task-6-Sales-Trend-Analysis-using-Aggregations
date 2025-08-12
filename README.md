# Task-6-Sales-Trend-Analysis-using-Aggregations

SELECT EXTRACT(...) AS ...: We use the EXTRACT() function to pull the $YEAR$ and $MONTH$ from the $order\_date$ column. We assign them clear aliases, $sales\year$ and $sales\month$, for readability.

SUM(amount) AS total_revenue: This calculates the sum of all values in the $amount$ column for each group, giving us the total monthly revenue.

COUNT(DISTINCT order_id) AS order_volume: This counts the number of unique $order\_id$ values in each group. Using $DISTINCT$ is crucial to ensure you are counting individual orders, not the number of products sold.

GROUP BY sales_year, sales_month: This is the core of the aggregation. It groups all the rows with the same year and month into a single summary row so that $SUM()$ and $COUNT()$ can operate on them.

ORDER BY sales_year, sales_month: This sorts the final output chronologically, first by year and then by month, which is essential for analyzing time-based trends.







