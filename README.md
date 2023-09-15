# CryptoClustering
Using the Crypto_Clustering.ipynb the script starts by using Standardscaler from scikit-learn to normalize the data in the dataset in the df_market_data.  
After normalizing the data, the script calls the function fit_transform() to transform and store df_market_data and store the scaled values in scaled_data, then creating a new data frame scaled_df, which keeps the column values and index from the original data frame. 
A range of K_values from 1 to 11 is created, representing the number of clusters(k) utilized in the K-means clustering.
An empty list is created to store the inertia values for each value of K, and a loop is created to iterate from the ranges of 1-11 for each value of K. 
The script utilizes the K and inertia values to plot and create the elbow_data dataframe and use that dataframe to visualize the line chart.
With the visualization of the line chart, we find the optimal k value and ensure reproducibility. The K-means model is then fitted to our scaled dataframe. Using the predict method, the script assigns cluster labels to the data points in the scaled dataframe and stores the labels in a 'cluster_labels.'
A copy of scaled data is created to store the new cluster labels 
A scatter plot visualization is created to visualize the clustering results using hvplots. 

The second part of this code uses PCA(Principal Component Analysis) 
The script sets the number of components to 3 and utilizes the fit_transforms method applied to the scaled dataframe. 
A new dataframe is created with the PCA-transformed scaled dataframe. 
Using a similar formula to the first part of the code, the code sets a range of K values from 1 to 12 and an empty list of inertia values and creates a similar loop to iterate the different values. But this time utilizing the PCA dataset as comparison.
Again, an elbow curve is plotted and K-means model is used but utilizing the PCA data frame.
The usage of PCA is used in conjunction as a comparison to see a possible difference in data and the visualization of a composition of the two elbow dataframes, one utilizing PCA and one not, the values the code finds in optimal K and elbow curve gives a same value with little to no variation.  
