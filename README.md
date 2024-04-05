# Indian-takeaway-data-analysis-project
![Indian-takeaway](img_takeaway/indian_takeaway2.jpg)

The Indian takeaway orders contains approx ~33k records from two restaurants in London between 2015 and 2019. This project provides valuable insights for the restaurants on the order details and sales to gain the business value. 

1.  Understanding the orders and menu from both the restaurants and getting the total cost based on quantity.
2.  Analysis of total quantity of each item ordered till date.
3.  Understanding the average count of each item ordered in a day.
4.  Finding the total sales of item sold till date and can be benefecial to generate the popular item by comparing the total quantity from above.
5. Average of items ordered in an order per day
6.  Count of orders on monthly basis to analyse the months with most order for the order trends.
7.  Generating average of order per month over the years.
8. orders generated on yearly basis.

# Python libraries to run the project:
1. *split* function for implementing the column split of order date and time.
2.  *to_date* and *DateType* for casting of date column from string to date format.
# How to use the project for gaining valuable insights
Using Databricks with pyspark for transformation and deriving values from the data.
# Data Cleaning and Manipulation:
PSB major points covered in Data cleaning and manipulation. Details are provided with code in the Databricks in notebook form.
1.  Loading the data for all the 4 csv's provided 
    1.  restaurant_1_orders.csv
    2.  restaurant_2_orders.csv
    3.  restaurant_1_products_price.csv
    4.  restaurant_2_products_price.csv
2.  To split the order date and time column using split function from pyspark for analysing the data w.r.t monthly and yearly basis.
3.  Changing the data types for both the restaurant order for date column to analyse the data for extracting the year and month.
4.  To calculate the total cost of each item based product quantity and product price details.
5.  *createOrReplaceTempView* - Creates or replaces a local temporary view with this DataFrame ,using the command generating the view of the files to process data using SQL.createOrReplaceTempView() is used when you wanted to store the table for a specific spark session.

# Business values using pyspark SQL:
PSB major points covered for gaining business value. Details with data is visible in notebook for each query. Insights and e.g. below are referring from restaurant1 data, for restaurant2 details are visible in the notebook.
1.  **Calculates the quantity of items ordered till date**: Helps to understand the total quantity of each item ordered till date in order to undestand the inventory to be kept and items required on daily basis, also helps to understand the least ordered item.
for e.g. based on the results, most ordered items are below, considering only 2. 
Plain Papadum  - 10648,
Pilau Rice     - 6367 
least ordered items are below:
Lamb Persian   - 1,
Mushroom - Prawn - 1
From above it will be easy to plan the inventory as well as the menu for future.
2.  **Average item quantity ordered in a day** : This data helps to understand the regularity of items on daily basis.
e.g. on average Plain Papadum has been ordered 8 times in a day and Lamb persian has been ordered 0.0008 times.
3.  **Calculates the total cost of item sold till date**: This is to understand the total sales generated from each item. 
e.g.: Chicken Tikka Masala - 22133.35,
Pilau Rice - 18782.65 has generated the most sales and can be considered as the popular dish for the restaurant1, likewise 
Tandoori Chicken - 8.95,
Chicken Chaat Main - 7.9 can be considered as least liked. 
4.  **Average item count ordered in an order for last 30 days**: data from this query is useful to understand the average count of items per order.
e.g.: each day on average item per order is 5 on a minimum basis and this threshold can help to decide the low and high priority of orders.
5.  **Total order for a month till date**: using this data trend can be analysed for monthly sales and it will help to plan the resources.
e.g. the most orders are in the month of July and June for 2019, the trend goes down and again takes peak in November and December.
6.  **Average order per month in a year**: similar to above this query provides the average of order yearly, helps to plan the resources.
e.g. here the most orders are from November and December on average:343.33 -11(Nov),
                    390 - 12(Dec)
7.  **Orders per year** : yearly trend of orders can be analysed and the growth in orders is visible for the restaurant1.
e.g: 2019 - 3270,
     2018 - 4553,
     2015 -29
8.  **Unique items in each restaurant** : Shows the unique items in each restaurant.
9.  **Common items in both the restaurants with price comparision** : compares the price for common items when the price differs for both restaurants, gives insights to check for reasonable price      

## Error handlings and failures:
The above conclusions and cleaning runs on the assumption that the data given in the price table and order table matches for the item name and product price.
In case the price value differs code still takes the price from the product price in orders table.




