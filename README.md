## Cases

Contains case studies

### Instructions

Predict the number of order days Do it for all the users that appear in the file 'august_with_missing_order_days.parquet'. 

Note : Your prediction is the remaining orders left for the month. If a user places 3 orders on the 10th, 20th, and 30th. 

We would want our predictions before the 10th to be 3, before the 20th to be 2, etc.

To do so, you can use the following:

* The already known orders in 'august_with_missing_order_days.parquet'.

* The file ' historical_orders.parquet ' contains the users' historical transaction (you should use it as a training set).

* The file 'august_total_sales.parquet ' contains the forecasted total transaction amount in August for each user. *You can assume that the forecasted value is accurate, and you can treat it as the true value for the total monthly sales - this information can help you make your predictions better but is not a must.

### Guidlines

You should submit 2 files:

* Submit a csv file with your predictions per user.

  * This prediction file should contain all the users in the file 'august_with_missing_order_days.parquet'

  * This file should contain 2 columns only - the first one is "account_id", the second one is "prediction". The shape of the file should be 32944 rows and 2 columns. The csv file should be called - “order_days_prediction.csv”.

  * [reminder] The column “prediction” should contain the number of order days left in the month. The file 'august_with_missing_order_days . parquet ' contains some days with orders. Do not consider those orders in the prediction - consider only the days left to order.

* Submit a python notebook (ipynb file) that shows all the steps that led to your prediction. We want to understand your thought process so make sure that this file contains all steps from EDA all the way to the final prediction.
