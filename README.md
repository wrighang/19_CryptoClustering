# 19_CryptoClustering

# Deliverable(s)

[Crypto_Clustering_starter_code.ipynb](https://github.com/wrighang/19_CryptoClustering/blob/main/Crypto_Clustering.ipynb)

## Background
In this challenge, I use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Requirements
### Find the Best Value for k by Using the Scaled DataFrame
To receive all points, you must:

- Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. <br/>
- **Question:** What's the best value for k?<br/>
   - **Answer:** The best value for `k` is the elbow point where `k` = 4. This is the point where adding more clusters does not significantly reduce inertia. 

### Cluster the Cryptocurrencies with K-Means by Using the Scaled DataFrame
To receive all points, you must:

- Initialize the K-means model with best value for k.
- Fit the K-means model by using the scaled DataFrame.
- Predict the clusters for grouping the cryptocurrencies by using the scaled DataFrame. Review the resulting array of cluster values.
- Create a copy of the scaled DataFrame, and then add a new column of the predicted clusters.
- Using `hvPlot`, create a scatter plot by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency that each data point represents.

### Optimize the Clusters with Principal Component Analysis
To receive all points, you must:

- Create a PCA model instance, and set `n_components=3.`
- Use the PCA model to reduce the features to three principal components.
- Get the explained variance to determine how much information can be attributed to each principal component.<br/>
- **Question:** What's the total explained variance of the three principal components?<br/>
   - **Answer:** 37.2% of the variance can be explained by the 1st principal component, the 2nd princiipal component is 34.7% and the 3rd principal component is 17.6%. The total explained variance is about 89.5%. <br/>
- Create a new DataFrame from the scaled PCA data. Be sure to set the `coin_id` index from the original scaled DataFrame as the index for the new DataFrame. Review the first five rows of the DataFrame.

### Find the Best Value for k by Using the PCA DataFrame
To receive all points, you must:

- Code the elbow method algorithm, and use the scaled PCA DataFrame to find the best value for k. Use a range from 1 to 11.
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.<br/>
- **Question:** What's the best value for k when using the scaled PCA DataFrame? Does it differ from the best value for k that you found by using the original scaled DataFrame?<br/>
   - **Answer:** When using the PCA data, the best value for `k` is the elbow point where `k` = 4. This is the point where adding more clusters does not significantly reduce inertia. No, it does not differ. Both elbow curves show `k` = 4. 

### Cluster the Cryptocurrencies with K-means by Using the PCA DataFrame
To receive all points, you must:

- Initialize the K-means model with the best value for k.
- Fit the K-means model by using the PCA data.
- Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values.
- Create a copy of the scaled PCA DataFrame, and then add a new column of the predicted clusters.
- Using hvPlot, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency that each data point represents.

### Visualize and Compare the Results
To receive all points, you must:

- Create a composite plot by using hvPlot and the plus sign (+) operator to compare the elbow curve that you created from the original scaled DataFrame with the one that you created from the scaled PCA DataFrame.
- Create a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original scaled DataFrame with those that resulted from the scaled PCA DataFrame.
- **Question:** Based on visually analyzing the cluster analysis results, what's the impact of using fewer features to cluster the data by using K-means?
   - **Answer:** In the original scatter plot, `crypto_cluster_scatter_plot`, the clusters were formed using more features, `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. The PCA scatter plot, `pca_scatter_plot`, uses clusters based on the first two principal compoenents, `x="PCA1"` and `y="PCA2"`. The PCA scatter plot is more condensed using the 2 PCA variables making it easier to visualize the clusters. While the elbow curve returned similar slopes, the PCA scatter plot of the 2 scatter plots is a better representation for analysis. Cryptocurrencies are affected by 24-hour or 7-day price changes since the clusters are grouped closely together it illustrates the shared similar behaviors in 24-hour and 7-day price changes. 

### Coding Conventions and Formatting
To receive all points, you must:

- Place imports at the top of the file, just after any module comments and docstrings, and before module globals and constants.
- Name functions and variables with lowercase characters, with words separated by underscores.
- Follow DRY (Don't Repeat Yourself) principles, creating maintainable and reusable code.
- Use concise logic and creative engineering where possible.

### Deployment and Submission
To receive all points, you must:

- Submit a link to a GitHub repository that's cloned to your local machine and that contains your files.
- Use the command line to add your files to the repository.
- Include appropriate commit messages in your files.

### Code Comments
To receive all points, your code must:

- Be well commented with concise, relevant notes that other developers can understand.


   ====================================================================
## CODING_PROCESS

- Referenced activity assignments and pdf slideshow throughout the challenge for reference. 
