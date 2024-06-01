### Case Study: Cryptocurrency Clustering Using Unsupervised Learning

#### Background

In this case study, we will explore the use of unsupervised learning techniques to analyze and cluster cryptocurrency data. The primary objective is to determine if cryptocurrencies can be grouped based on their 24-hour and 7-day price changes. This project was carried out for the United States Geological Survey (USGS) to visualize data in a meaningful way and potentially secure funding for further research.

#### Project Overview

1. **Repository Setup**
    - Created a new repository called `CryptoClustering`.
    - Cloned the repository to the local machine.
    - Pushed the changes to GitHub.

2. **Data Preparation**
    - Loaded the `crypto_market_data.csv` into a DataFrame.
    - Examined summary statistics and visualized the initial data distribution.

3. **Data Normalization**
    - Utilized `StandardScaler` from scikit-learn to normalize the data.
    - Created a new DataFrame with the scaled data, setting the "coin_id" as the index.

4. **Finding the Optimal k**
    - Employed the elbow method to determine the best value for k.
    - Generated inertia values for k ranging from 1 to 11.
    - Plotted the elbow curve to visually identify the optimal k value.

5. **Clustering with K-means**
    - Used K-means clustering to group cryptocurrencies based on the optimal k value.
    - Created a scatter plot using hvPlot to visualize the clusters.

6. **Dimensionality Reduction with PCA**
    - Reduced the features to three principal components using PCA.
    - Analyzed the explained variance to understand the information retained in the principal components.
    - Created a new DataFrame with the PCA data.

7. **Re-evaluating the Optimal k with PCA Data**
    - Applied the elbow method on the PCA data to find the optimal k value.
    - Compared the optimal k values obtained from the original and PCA data.

8. **Clustering with PCA Data**
    - Clustered the PCA data using K-means based on the new optimal k value.
    - Visualized the clusters using a scatter plot in hvPlot.

#### Detailed Analysis

##### Data Preparation and Normalization

The initial step involved loading and examining the `crypto_market_data.csv` file. Summary statistics and data visualizations were generated to understand the data distribution.

To normalize the data, the `StandardScaler` from scikit-learn was applied, resulting in a scaled DataFrame. This step ensures that each feature contributes equally to the analysis.

##### Finding the Optimal k

Using the elbow method, we determined the best value for k, which is crucial for K-means clustering. The inertia values were computed for k ranging from 1 to 11, and an elbow curve was plotted to visually identify the optimal k value. The best value for k was selected based on the point where the inertia values start to level off.

##### Clustering with K-means

With the optimal k value, the K-means model was initialized and fitted using the scaled DataFrame. A scatter plot was created using hvPlot to visualize the clusters. This plot helps in understanding how cryptocurrencies are grouped based on their 24-hour and 7-day price changes.

##### Dimensionality Reduction with PCA

To reduce the complexity of the data, PCA was performed, reducing the features to three principal components. The explained variance was analyzed to determine the amount of information retained. A new DataFrame was created with the PCA data, setting the "coin_id" as the index.

##### Re-evaluating the Optimal k with PCA Data

The elbow method was reapplied to the PCA data to find the optimal k value. This step helps in understanding if the dimensionality reduction impacts the optimal k value. The new optimal k value was compared with the one obtained from the original data.

##### Clustering with PCA Data

Using the new optimal k value, the K-means model was fitted with the PCA data. The clusters were visualized using a scatter plot in hvPlot, displaying the clusters based on the principal components.

#### Conclusion

This project demonstrates the use of unsupervised learning techniques to cluster cryptocurrencies based on their price changes. The process of finding the optimal k value, clustering with K-means, and visualizing the results provides valuable insights into the data. Dimensionality reduction with PCA further simplifies the data, making it easier to analyze and interpret.

The impact of using fewer features was analyzed, showing how dimensionality reduction can help in clustering without significant loss of information. This case study highlights the practical application of machine learning techniques in the field of data science and their potential to uncover meaningful patterns in large datasets.

#### Resources

To successfully complete this project, a variety of resources were utilized:

- **Documentation:**
  - [scikit-learn Documentation](https://scikit-learn.org/stable/user_guide.html): Provided guidance on using `StandardScaler` for data normalization and `KMeans` for clustering.
  - [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/): Used for data manipulation and analysis.
  - [hvPlot Documentation](https://hvplot.holoviz.org/): Assisted in creating interactive visualizations.

- **Stack Overflow:**
  - Various discussions and solutions related to data preprocessing, clustering, and visualization were referred to from Stack Overflow to troubleshoot and optimize the code.

- **Past Assignments:**
  - Techniques and methodologies from previous assignments on clustering, PCA, and data visualization were applied and adapted for this project.

By leveraging these resources, the project was completed efficiently, ensuring robust and accurate analysis and visualization of the cryptocurrency data.
