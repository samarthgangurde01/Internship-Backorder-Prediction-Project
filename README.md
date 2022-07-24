
# Project Title:- Backorder Prediction
[https://images.indianexpress.com/2018/07/10_759-1.jpg](https://i.pcmag.com/imagery/articles/03CMc2DfBSZ0x9ZZPfNfh0T-3.fit_scale.size_1028x578.v1590500207.jpg)
## Description
It was intership project from ineuron.ai
problem statement-Backorders are unavoidable, but by anticipating which things will be backordered, 
planning can be streamlined at several levels, preventing unexpected strain on 
production, logistics, and transportation. ERP systems generate a lot of data (mainly 
structured) and also contain a lot of historical data; if this data can be properly utilized, a 
predictive model to forecast backorders and plan accordingly can be constructed. 
Based on past data from inventories, supply chain, and sales, classify the products as 
going into backorder (Yes or No).
Solution:-Our imported dataset had 1687860 rows and 23 columns. when we started analyzing out of 23 columns 2 columns local_bo_qty and pieces_past_due had 98% missing values we romved those variables,also had one variable with missing values 100894 replace them with median
after cleaned data we performed EDA where we found that variables like fore_cast_3_month, fore_cast_6_month, fore_cast_9_month
sales_1_month,sales_3_month sales_6_month sales_9_month,perf_6_month_avg were highly correalted to each other we kept first of them and removed remaining variables
Used one hot encodeing for the categorical variables,used min max scaler to scale down the variables
as our dataset had outliers and was imbalanced. capped the outliers by IQR range and SMOTE technic to balance dataset.Used logistic regression,kneighbors classifier
decision tree classifier,random forest classifier and voting classifier with hyperparameter tunning to train the model

## Table of Content
* Description
* Dataset Information
* Tools and Libraries Used
* Files
* Results
* Screenshots
* feedback

## Dataset Informatio
In the Train dataset we are provided with 23 columns(Features) of data.

* Sku(Stock Keeping unit) : The product id — Unique for each row so can be ignored

* National_inv : The present inventory level of the product

* Lead_time : Transit time of the product

* In_transit_qty : The amount of product in transit

* Forecast_3_month , Forecast_6_month , Forecast_9_month : Forecast of the sales of the product for coming 3 , 6 and 9 months respectively

* Sales_1_month , sales_3_month ,sales_6_month , sales_9_month : Actual sales of the product in last 1 , 3 ,6 and 9 months respectively

* Min_bank : Minimum amount of stock recommended

* Potential_issue : Any problem identified in the product/part

* Pieces_past_due: Amount of parts of the product overdue if any

* Perf_6_month_avg , perf_12_month_avg : Product performance over past 6 and 12 months respectively

* Local_bo_qty : Amount of stock overdue

* Deck_risk , oe_constraint, ppap_risk, stop_auto_buy, rev_stop : Different Flags (Yes or No) set for the product

* Went_on_backorder : Target variable(Products that went to Backorder(‘Yes’) to those which didn’t go to Backorder(‘No’)



## Files
* Backorder Prediction.pdf:-Pdf containing Problem statement and tasks
* Dataset:-Dataset with 1687860 rows and 23 columns
* Cleaned data:-Preprocessed data
* ineuron_project.ipynb:-Project colab 

##Some of the screen shorts from EDA
![image](https://user-images.githubusercontent.com/93859458/180659491-5f0e2dda-0af5-49e8-b179-c5fef71415b6.png)
![image](https://user-images.githubusercontent.com/93859458/180659530-a7943780-72fa-4361-88f6-8760cde1d70d.png)
![image](https://user-images.githubusercontent.com/93859458/180659575-e31b7eab-19df-40ee-a8aa-18898800e681.png)
![image](https://user-images.githubusercontent.com/93859458/180659590-4c94ab5e-dcd7-40c4-b5b2-5a4f9762b530.png))
![image](https://user-images.githubusercontent.com/93859458/180659617-b4aa4bfb-118e-4ac3-89f8-0a707cb6fbc4.png)
![image](https://user-images.githubusercontent.com/93859458/180659635-27107e27-fbe6-4b82-8c88-60526e096b33.png)


## Results
We have used 5 algorithsm to train model where algorithsm
# Logistic Regression gave us
![image](https://user-images.githubusercontent.com/93859458/180659718-7ba69d67-9f96-4c0a-b8bc-32be5264f2a4.png)
# Decision tree classifier gave us
![image](https://user-images.githubusercontent.com/93859458/180659817-1a864ef1-476e-4888-afd8-927caacd044b.png)

## Feedback

If you have any feedback, please reach out to us at samarthgangurde01@gmail.com


