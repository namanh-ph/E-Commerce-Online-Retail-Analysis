# Online Retail Analysis - E-Cpmmerce

## 1. Introduction

### 1.1. Background

For this project, let's take a look at the data of a UK-based online retailer from 2010-2011 containing information related to the transactions made from 2010 to 2011. The task is to discover important information about the sales so that the store can improve upon, and classify the customers into different types in order to approach them appropriately with different strategies.

This data consists of over 500,000 records of customer orders, including 8 variables that correspond to:

* InvoiceNo: Invoice number
* StockCode: Product code
* Description: Product name
* Quantity: The quantities of the product each transaction
* InvoiceDate: Invoice Date and time
* UnitPrice: Price per unit
* CustomerID: Customer number
* Country: The country where each customer resides

### 1.2. Objectives

This case study will focus on exploring the data and extracting important insights:

* Exploratory Data Analysis (EDA)
* RFM Analysis: find out the customers' RFM features (Recency, Frequency, Monetary)
* Customer classification based on their RFM information: K-Means Clustering and Hierarchical Clustering Model

### 1.3. Tool used

Python:

* Data cleaning and preparation
* Exploratory Descriptive Analysis (EDA)
* Recency-Frequency-Monetary (RFM) Analysis
* Clustering models: K-Means and Hierarchical Clustering

## 2. Result

### 2.1. Analysis

#### 2.1.1. Customers

* Domestic buyers (UK buyers) accounted for the majority of the sales, and this would be the store's main type of customer to perform more campaigns.
* From September, there was a burst of new customers, and in November the number of new customers more than tripled that of last year. The reason needs to be found so that the store may replicate this success.

#### 2.2.2. Sale Status

* Most of the sale are from domestic buyers.
* Top products of the time are: White Hanging Heart T-Light Holder, Jumbo Bag Red Retrospot, and Regency Cakestand 3 Tier.
* Towards the end of the year, as a lot of new customers came to the store, the number of order also witness an upturn.
* Although a transaction usually had a moderate amount of quantity, the revenue order was only less than 25 GBP per order, which is not very high.

### 2.2. Clustering Models & Customer Groups

Based on the means of 3 features: Recency, Frequency, Monetary, as well as the group of K-Means and Hierarchical Clustering, the customers can be devided into 6 groups.

![Model Comparison](https://github.com/nam-anh-21/E-Commerce-Online-Retail-Analysis/blob/main/Model%20Comparison.png)

(*): Slight difference between the grouping of 2 models

#### Group 1: Champion

* K-Means Cluster 4 and Hierarchical Cluster 1
* Very low Recency, high Frequency, and very high Monetary value
* This group is easily the the most profitable group.

#### Group 2: Loyal

* K-Means Cluster 2 and Hierarchical Cluster 3
* Very low Recency, very high Frequency, and high Monetary value
* These customers buy the most with a large figure of Frequency.


#### Group 3: Potential

* K-Means Cluster 0 and Hierarchical Cluster 2 (*)
* Low Recency, moderate Frequency, and moderate Monetary value
* This type of customer is promising. With a bit of encouragement via marketing campaign to attract them more, they could generate more profit for the store.

#### Group 4: Standard

* K-Means Cluster 3 and Hierarchical Cluster 4 (*)
* Moderate Recency, moderate Frequency, and moderate Monetary value
* These buyers take up the largest proportion of all customers, with moderate numbers in all features. They make up the dominant behaviour of customers of this store.

#### Group 5: At Risk

* K-Means Cluster 5 and Hierarchical Cluster 0 (*)
* High Recency, low Frequency, and low Monetary value
* This group of customers has not made any purchase in recent time, while making low purchases. Their value to the store is low and they need some attention.

#### Group 6: Dormant

* K-Means Cluster 1 and Hierarchical Cluster 5
* Very high Recency, very low Frequency, and very low Monetary value
* There are those who have yet to make any purchase lately, but also did not make many purchases and spent little money. It seems to be unlikely that they will make any purchase from the store again.
