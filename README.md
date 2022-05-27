# Cryptocurrencies, Module 18 Challenge

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.
The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.


## Deliverable 1: Preprocessing the Data for PCA

Cryptocurrencies that are "not being traded" were removed.

![11](Images/11.png)

The "IsTrading" column was dropped.

![12](Images/12.png)

All the rows that have "at least one null value" were removed.

![13](Images/13.png)

All the rows that "do not have coins being mined" were removed.

![14](Images/14.png)

The "CoinName" column was dropped.

![15](Images/15.png)

A new DataFrame was created that stores "all cryptocurrency names from the CoinName column" and retains the index from the crypto_df DataFrame.

![16](Images/16.png)

The "get_dummies() method" was used to create variables for the text features, which are then stored in a new DataFrame, X.

![17](Images/17.png)

The features from the X DataFrame were standardized using the "StandardScaler fit_transform() function".

![18](Images/18.png)


## Deliverable 2: Reducing Data Dimensions Using PCA

You will earn a perfect score for Deliverable 2 by completing all requirements below:
The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components (10 pt)
The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame (10 pt)


## Deliverable 3: Clustering Cryptocurrencies Using K-means

You will earn a perfect score for Deliverable 3 by completing all requirements below:
The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
An elbow curve is created using hvPlot to find the best value for K (10 pt)
Predictions are made on the K clusters of the cryptocurrencies’ data (5 pt)
A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class (5 pt)


## Deliverable 4: Visualizing Cryptocurrencies Results

You will earn a perfect score for Deliverable 4 by completing all requirements below:
The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover (10 pt)
A table with tradable cryptocurrencies is created using the hvplot.table() function (3 pt)
The total number of tradable cryptocurrencies is printed (2 pt)
A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns (5 pt)
A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point (10 pt)
