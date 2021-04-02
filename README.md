# Unsupervised Machine Learning for Cryptocurrencies

## Overview

Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. Given a list of available cryptocurrencies and information such as trading status, total coins mined and total coin supply, we aimed to develop an unsupervised machine learning model to report cryptocurrencies that are on the trading market and how they could be grouped towards creating a classification for developing this new investment product.

# Technologies

- Python
- Jupyter Notebook
- Pandas
- Sklearn (StandardScaler, PCA, AgglomerativeClustering, KMeans)
- Hvplot
- Plotly

# Processing and Analysis

### 1) Preprocessing the Data for PCA

- Kept only the cryptocurrencies that are being traded, have a working algorithm, and where coins have been mined.
- Droped the IsTrading column.
- Removed rows that have at least one null value.


### 2) Reducing Data Dimensions Using PCA

- Reduced the dimensions of the X DataFrame down to three principal components. 
- Clustered Cryptocurrencies using K-means
- Created an elbow curve using hvPlot to find the best value for K 
- Using the Elbow curve, it is determined that ideal number of clusters would be 4.

### 3) Visualizing Results

- A 3D-Scatter plot with the PCA data and the clusters looks like:

![PCA](https://github.com/MariaGarzon/Cryptocurrencies/blob/ed2ad67d174b25bdd0809f5d7b3f4caf85542bba/Visuals/PCA.png)

- Further a scatter plot to contrast the number of available coins versus the total number of mined coins was created: 

![bokeh plot](https://github.com/MariaGarzon/Cryptocurrencies/blob/ed2ad67d174b25bdd0809f5d7b3f4caf85542bba/Visuals/bokeh_plot.png)

## Summary 

There are a total of 532 tradable cryptocurrencies that were grouped into four clusters. The clusters fall into the following categories:

1) High supply, low demand
2) Medium supply, low demand
3) Low supply, low demand
4) High supply, high demand
