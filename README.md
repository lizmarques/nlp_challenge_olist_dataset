<h1 align="center"> NLP Challenge using Olist Dataset </h1>

## Links

- Google Colab Notebook - [NLP_Challenge_Olist_Dataset.ipynb](https://github.com/lizmarques/nlp_challenge_olist_dataset/blob/207e3e0fd4f7a2afceb378d8eb0479bf69ea0aea/NLP_Challenge_Olist_Dataset.ipynb)

## Data Source: Olist

This is a Brazilian ecommerce public dataset of orders made at Olist Store. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. There is also a geolocation dataset that relates Brazilian zip codes to lat/lng coordinates.

This is real commercial data, it has been anonymised, and references to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses. (source: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## Data exploration
### Review Score vs Quantity

Through this bar plot, we can conclude that the majority of reviews have a rating of 5, i.e. the maximum grade

<p align="center"> <img width="500px" heigth="200px" src="images/review_score_vs_quantity.png">

#### Note 1
As the goal of this challenge is to build a classification model, we will need to create one more column that will be our class. Therefore, we will establish that:
"review_score" less than or equal to 3, will be classified as negative (receiving the value 0)
"review_score" greater than or equal to 4, will be classified as positive (receiving the value 1)

### Class vs Quantity

Here we can see that our database is unbalanced, since there are more positive records than negative ones.
As the calculations below show, we can see that positive records(1) correspond to 65.7% of the total database, against 34.3% of negative records (0).
     
 - Class 0: 8.479
 - Class 1: 16.243

<p align="center"> <img width="500px" heigth="200px" src="images/class_vs_quantity.png">
