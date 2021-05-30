## Query - 1 : What is the total amount each customer spent at the restaurant?

```select s.customer_id , SUM(m.price) as Total_Amount_Spent  
FROM sales AS s JOIN menu AS m  ON s.product_id = m.product_id 
GROUP BY s.customer_id 
ORDER BY s.customer_id; 
```
## Output - 
![week1-code1](https://user-images.githubusercontent.com/28923252/120117107-3ce1d900-c1a9-11eb-8369-542f58fa843a.PNG)


## Query - 2 : How many days has each customer visited the restaurant?

``` select customer_id, COUNT(order_date) AS Days_Visited 
FROM sales 
GROUP BY customer_id 
ORDER BY customer_id;
```
## Output - 
![image](https://user-images.githubusercontent.com/28923252/120117778-6fd99c00-c1ac-11eb-9093-7b26a9ece053.png)
