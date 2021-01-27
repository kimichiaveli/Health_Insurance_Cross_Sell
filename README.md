# Janatahack: Cross-sell Prediction

Welcome to my second project, this is my work for Janatahack: Cross-sell Prediction on [Analytics Vidhya](https://datahack.analyticsvidhya.com/contest/janatahack-cross-sell-prediction/)

## Overview

Cross-selling identifies products or services that satisfy additional, complementary needs that are unfulfilled by the original product that a customer possesses. As an example, a mouse could be cross-sold to a customer purchasing a keyboard. Oftentimes, cross-selling points users to products they would have purchased anyways; by showing them at the right time, a store ensures they make the sale.

Cross-selling is prevalent in various domains and industries including banks. For example, credit cards are cross-sold to people registering a savings account. In ecommerce, cross-selling is often utilized on product pages, during the checkout process, and in lifecycle campaigns. It is a highly-effective tactic for generating repeat purchases, demonstrating the breadth of a catalog to customers. Cross-selling can alert users to products they didn't previously know you offered, further earning their confidence as the best retailer to satisfy a particular need.

In this case, we are tasked to cross-sell our vehicle insurance product to people who bought our health insurance. But we can't just pitch everyone into buying them because it will be time consuming. So, how do we know which one we have to ask to buy the insurance?

## Approach

By creating Machine Learning model to predict customer's response, we could :

1. Maximize revenue by capturing all of the market share
2. Cut the time and cost of selling those insurance

Also, by exploring our data we could gain new insight of our customer's behaviour.

## EDA

**Here's the features correlation heatmap, notice that 'Previously_Insured' has the highest correlation on the 'Response'**<br>
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/heatmapcorr.png 'Correlation Heatmap')
**Pretty sure that only people who currently don't have vehicle insured will response positively**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/previnsured.png 'Previously_Insured countplot')
**Here we can see how the vehicle age and damage distribution based on their response**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/vehage.PNG 'Vehicle Age based on the response')
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/vehcomp.PNG 'Vehicle Composition')
**Classification Metrics of CatBoost model (without SMOTE or class-weight)**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/defmetric.PNG)
**Classification Metrics of CatBoost model with SMOTE (oversampling method)**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/smotemetric.PNG)
**Classification Metrics of CatBoost model with auto-balanced class weight**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/classweightmetric.PNG)
**Confusion Matrix of CatBoost model with SMOTE**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/consmote.png)
**Confusion Matrix of CatBoost model with auto-balanced class weight**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/conclassweight.png)
**ROC-AUC plot CatBoost model with SMOTE**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/rocaucsmote.png)
**ROC-AUC plot CatBoost model with auto-balanced class weight**
![alt text](https://github.com/kimichiaveli/Health_Insurance_Cross_Sell/blob/main/rocaucclassweight.png)
