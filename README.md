# CryptoClustering![Alt text](download-1.jpg)

The file Crypto_Clustering.ipynb was created to use unsupervised machine learnig to predict if cryptocurrencies are affect by 24-hour or 7-day price changes .

The crypto_market_data.csv was loaded into a DataFrame.

Initial summary statistics were ran and a plot was created from the data to see what the data looks like before proceeding.

## Prepare the Data

The data was prepared using the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

A DataFrame was created using the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the best Value for K

The Best Value was found for k Using the Original Scaled DataFrame and then the elbow method was used to find the best value for k, which was 4.

## Cluster Cryptocurrencies with K-means

The Cryptocurrencies were clustered to find the best value for k using the original scaled data. A scatter plot using hvPlot was created to visualize the clusters from the K-means model.

## Optimize Clusters with Principal Component Analysis

Using the original scaled DataFrame, PCA was used to reduce the features to three principal components. PCA1, PCA2 and PCA3.

A new DataFrame was created utilizing the PCA data and the "coin_id" was set as the index from the original DataFrame for the new DataFrame

## Find the Best Value for k Using the PCA Data

The elbow method was ran using the PCA data to find the best value for k. A line chart was ploted with all the inertia values computed with the different values of k to visually identify the optimal value for k, which was determined to be 4.

## Cluster Cryptocurrencies with K-means Using the PCA Data

The cryptocurrencies were clustered for the best value for k on the PCA data using the K-kmeans model.

A copy of the DataFrame with the PCA data was made and a new column to store the preidicted clusters was added. A new scatter plot was created using hvPlot the graph point colored with labels found using K-means.

In this instance; the impact of using fewer features to cluster the data using K-means provided simplicity in interpretability and is efficent for computation. The line plots for the elbow curve is a steeper inertia drop, even though the k value was the same for both plots. When analyzing the scatter plots for cluster predictions, using fewer features resulted in tighter clusters and more entries within cluster 0 and cluster 1.
