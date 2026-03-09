SELECT
    geography,
    COUNT(*) AS customers,
    SUM(exited) AS churned_customers,
    ROUND(100.0 * SUM(exited) / COUNT(*),2) AS churn_rate
FROM customers_clean
GROUP BY geography
ORDER BY churn_rate DESC;

