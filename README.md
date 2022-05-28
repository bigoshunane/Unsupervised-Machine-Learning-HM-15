# Cryptocurrency Clusters

## Project objective

The aim of this project is to use unsupervised machine learning to analyze a database of cryptocurrencies and create a report including the traded cryptocurrencies classified by group according to their features. The classification report will be for investment bank to propose a new cryptocurrency investment portfolio to its customers.

The original cryptocurrency data from CryptoCompare is preprocessed using Pandas to fit into Unsupervised Machine Learning models. A clustering algorithm is used to group the cleaned data and hvPlot visualization are used to show results.

The following methos applied to the given raw data:

   . Database preprocessing, details found in juypternotebook file named [cryptocurrency_cluster.ipynb](https://github.com/bigoshunane/Unsupervised-Machine-Learning-HM-15/blob/main/cryptocurrency_cluster.ipynb) in this repository.
                    
   . Reducing the data dimension using Principal Component Analysis,
         
   . Clustering cryptocurrencies using K-Means and
 
   . Visualizing classification results with 2D and 3D scatter plots.

## Data Source

 https://min-api.cryptocompare.com/data/all/coinlist  and https://www.cryptocompare.com/coins/list/all/USD/1
 
## Technologies used

  . Python 
  
  . scikit-learn 
  
  . hvPlot 
  
  . Plotly 

## Results

1. Clustering Cryptocurrencies using K-Means - Elbow Curve

Since the output of the analysis is not known unsupervised machine learning is used to identify clusters of the cryptocurrencies.
The elbow curve below using the K-Means method iterating on k values from 1 to 10 was used resulting in the following figure with the best K value appearing to be 4; hence, it can be concluded that catagorizing cryptocurrencies in to 4 clusters is feasible. 
 
<img width="1007" alt="elbow" src="https://user-images.githubusercontent.com/84547558/167717810-6ef5ff28-54c7-4cdf-9752-723077419ea6.png">

2. Visualizing Cryptocurrencies Results

2.1 3D-Scatter plot with clusters

This 3-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to three principal components.

![3d](https://user-images.githubusercontent.com/84547558/167718025-459941a5-8c79-4711-8b24-d45bb907180e.png)

2.2 hvPlot (Table)

The hvTable displaying all current tradeable cryptocurrencies. The Class column identifies the cluster to which the coin belongs. This table is created using the hvplot.table()function.

<img width="1011" alt="table" src="https://user-images.githubusercontent.com/84547558/167718342-9cab41ea-425c-4363-be04-533d2916a3df.png">


2.3 hvPlot (Scatter)

Scatter plot from two cryptocurrency features Using the PCA algorithm is the best method for better visualizations as shown in figure below: 
2D-Scatter plot with TotalCoinMined vs TotalCoinSupply.

<img width="1006" alt="2dscatterplot" src="https://user-images.githubusercontent.com/84547558/167719037-24ac9272-4dc5-4940-8e15-a1b679f0511f.png">

2.4 hvPlot (Scatter) 
PC1 VS PC2
<img width="1005" alt="PC1VS2" src="https://user-images.githubusercontent.com/84547558/167719643-e3339b82-4f7a-41bb-8c58-57fe5e6e644a.png">

## Summary
Based the analysis conducted about 532 cryptocurrencies have been identified based on similarities of their features. 
It would appear that splitting up the coins into four clusters was quite appropriate. The clusters fall into the following categories:

. High supply, low demand

. Medium supply, low demand

. Low supply, low demand

. High supply, high demand

Based on this statistics, together with more information about the companies issuing these coins and their price history it would be very instructive in determining the cluster of currencies into which it would be more reasonable to invest in. Particularities of each group need to be analyzed to determined their performance and potential interest for the investment bank's customers.


## References
Crypto Coin Comparison Ltd. (2020) Coin market capitalization lists of crypto currencies and prices. Retrieved from https://www.cryptocompare.com/coins/list/all/USD/1

© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
