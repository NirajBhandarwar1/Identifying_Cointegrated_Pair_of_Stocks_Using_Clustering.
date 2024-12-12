
# Identifying Cointegrated Pairs of Stocks Using Clustering


## Overview
This project aims to identify cointegrated pairs of stocks from the S&P 500 dataset using clustering algorithms. Cointegrated pairs are stocks whose prices exhibit a long-term equilibrium relationship, which can be leveraged for statistical arbitrage strategies. The project employs various clustering techniques to group similar stocks and identifies pairs with high cointegration.

## Key Highlights
- Dataset:
  - Utilized the S&P 500 dataset containing stock price data.
  - Performed data cleaning and feature engineering to prepare the dataset for clustering.
- Data Preprocessing:
  - Conducted Exploratory Data Analysis (EDA) to understand data trends and patterns.
  - Standardized features using StandardScaler for improved clustering performance.
- Clustering Algorithms:
  - Implemented three clustering techniques:
    - K-Means Clustering
    - Hierarchical Clustering
    - Affinity Propagation
- Determined the optimal number of clusters using the following:
  - Elbow Method for K-Means.
  - Dendrogram for Hierarchical Clustering.
- Results:
  - Achieved a top silhouette score of 0.35 with Affinity Propagation, outperforming other clustering methods.
  - Identified 32 cointegrated pairs among 47 unique stocks, providing a foundation for statistical arbitrage strategies.


## Dependencies
To run this project, the following Python libraries are required:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy
## Methodology
- Data Preprocessing:
  - Cleaned and standardized the stock price data using StandardScaler.
  - Performed EDA to visualize stock trends and understand feature distributions.
- Clustering:
  - Applied K-Means Clustering with the Elbow Method to find the optimal number of clusters.
  - Visualized Hierarchical Clustering results using a dendrogram to validate the cluster structure.
  - Implemented Affinity Propagation, which automatically determines the number of clusters and achieves the highest silhouette score.
- Pair Identification:
  - Within each identified cluster, calculated cointegration scores for stock pairs were calculated.
  - Selected pairs with high cointegration for further analysis.
- Evaluation:
  - Evaluated clustering performance using the silhouette score.
  - Validated cointegrated pairs based on statistical properties and clustering results.

## Results

- Affinity Propagation achieved the highest silhouette score of 0.35, effectively identifying clusters with cointegrated stock pairs.
- From the clustering results, 32 cointegrated pairs were identified among 47 unique stocks.
## Conclusion
This project demonstrates the application of clustering techniques to identify cointegrated stock pairs. The results highlight the effectiveness of Affinity Propagation in clustering stocks for this purpose. These cointegrated pairs can serve as a starting point for developing statistical arbitrage strategies.
## Future Improvements

- Perform additional statistical tests (e.g., Augmented Dickey-Fuller test) to verify cointegration of identified pairs.
- Explore advanced clustering methods such as DBSCAN or Gaussian Mixture Models.
- Integrate the clustering pipeline with real-time stock data for live trading applications.