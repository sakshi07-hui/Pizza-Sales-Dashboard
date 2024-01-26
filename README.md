THESE ARE THE QUERIES WHICH ARE USED IN THIS PARTICULAR PROJECT...
select * from pizza_sales
1.select sum(total_price) as total_revenue from pizza_sales

2. select sum(total_price)/count(distinct order_id) as avg_order_value from pizza_sales

3. select sum(quantity) as total_pizza_sold from pizza_sales

4.select count(distinct order_id) as total_orders from pizza_sales

5. select cast(cast(sum(quantity) as decimal(10,2)) /
 cast(count(distinct order_id) as decimal(10,2)) as decimal(10,2)) as avg_pizzza_perorder
 from pizza_sales
 
6.select to_char(order_date,'day') as order_day ,count(distinct order_id) as total_orders
from pizza_sales
group by order_day

7. select to_char(order_date,'month') as month_name, count(distinct order_id) as total_orders
   from pizza_sales
   group by month_name order by total_orders desc
   
8. select pizza_category,sum(total_price) as total_sales,sum(total_price) * 100 /(select sum(total_price) 
   from pizza_sales) PCT
   from pizza_sales
   group  by pizza_category
   
9. select pizza_size,sum(total_price) as total_sales,sum(total_price) * 100 /(select sum(total_price) 
   from pizza_sales) PCT
   from pizza_sales
   group  by pizza_size order by pct desc
   
10.select pizza_name,sum(total_price) as total_revenue from pizza_sales
   group by pizza_name order by total_revenue desc limit 5
   
11.select pizza_name,sum(total_price) as total_revenue from pizza_sales
   group by pizza_name order by total_revenue asc limit 5
   
12.select pizza_name,sum(quantity) as total_quantity from pizza_sales
   group by pizza_name order by total_quantity desc limit 5
   
13.select pizza_name,sum(quantity) as total_quantity from pizza_sales
   group by pizza_name order by total_quantity asc limit 5
   
14.select pizza_name,count(distinct order_id) as total_orders from pizza_sales
   group by pizza_name order by total_orders desc limit 5
   
15. select pizza_name,count(distinct order_id) as total_orders from pizza_sales
   group by pizza_name order by total_orders asc limit 5
   
