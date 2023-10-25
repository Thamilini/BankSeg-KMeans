# Bank Customer Segmentation with K-means Clustering

This is personal portfolio project by Thamilini P.

### Datasets Source

This case study analysis uses the "Clustering-Bank Dataset" from [Kaggle](https://www.kaggle.com/datasets/gopi1035/clusteringbank-dataset?). This dataset contains customer and branch details for a leading retail bank in India. The bank aims to use customer segmentation to improve their customer services (i.e.the wait times and frequency of marketing emails). 

### Task/Objectives

- Segment bank customers into clusters based on their demographics and relationship with the bank. 
- Identify high-value customers within the segmentation to provide them with priority service. 
- Leverage insights from clusters to better understand customers and develop personalized marketing.   

## Methodology

The datasets were cleaned, processed and transformed using R. The following libraries were used:
* tidyverse
* skimr
* janitor
* lubridate
* ggplot2

### Phases

* Ask Phase
    - Define Task/Objectives
* Prepare Phase
    - Import dataset as Dataframe
    - Datatypes and Descriptive Statistics
* Process Phase
    - Missing Values
    - Duplicate Values
    - Outliers
    - Create and Transform Columns 
* Analyze Phase
    - Standardize Dataset
    - Determine Optimal K Clusters (Elbow Plot)
    - Perform K-Means Clustering
    - Cluster Analysis
    - Cluster Insights
    - Identify High-Value Customers Cluster
    - Personalized Marketing Recommendations

### K-means clustering

This project uses K-means clustering to segment customers into clusters. K-means clustering groups similar data into clusters using euclidean distance. i.e. it uses the principle that similar points have smaller euclidean distance. First we determined the optimal number of K clusters using an Elbow Plot. The we performed k-means cluster using the kmeans() function in R. This function performed the following steps:

1. Randomly Pick k Centroids/Centers
2. Assign each data point to the centroid its closest to (determined by euclidean distance) forming cluster
3. Compute new centroid of each cluster (by calculating the mean of each cluster)
4. Repeat steps 2 and 3 several times (choosing a new centroid and assignment data points) until cluster memberships no longer change (i.e. the Sum of Squared Errors (SSE) between the data points and centroid is minimized).

![A graphical look at k-means clustering](https://ds055uzetaobb.cloudfront.net/brioche/uploads/y4KGN92h7r-screen-shot-2016-05-05-at-43007-pm.png?width=1200)


