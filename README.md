## Credit Card Clustering Project - Overview:
In this project, I attempt to split a credit card dataset I obtained through Kaggle into clusters and give the customers appropriate labels which could 
be used toward business decisions or marketing efforts.

* After ingesting the data, I performed some data cleaning by checking for null values and ensuring columns had appropriate data types.

* I then performed EDA by using correlation and bivariate analysis techniques. As one would expect, those with higher balance had a higher credit limit, and just about 
all frequency attributes were positively correlated with their general attribute counterpart.

* Applied K-Means and PCA to the data in attempt to create appropriate clusters based on the data. 

* Using a scree plot/elbow method, I elected to use 4 clusters to split the data, and found that 4 clusters represented the data fairly well.


## Code and Resources Used:

**Python Version:** 3.8.5

**Packages:** numpy, pandas, matplotlib, seaborn

## References:

* Knowledge behind PCA and K-Means clustering I originally learned and applied by taking a course from the following resource:
https://learn.365datascience.com/

## Data Collection:

* The data used for this project comes from Kaggle at the following link:
https://www.kaggle.com/datasets/arjunbhasin2013/ccdata


## Data Cleaning

After collecting the data, I dropped the few records that contained NaN values from the data since there were so few. Following this, I checked the data types of the
columns to ensure they were numeric in order for techniques such as K-Means to be applied to the data.


## EDA
When conducting EDA, there was an intuitive connection and positive correlation between balance and credit limit. I also created a dendrogram based on the data which 
also found approximately 4 high level clusters. I used this as an additional factor when deciding the final amount of clusters to use with K-Means.

![alt text](https://github.com/elayer/CreditCardClusteringProject/blob/main/creditlim_bal.png "Balance vs. Credit Limit")
![alt_text](https://github.com/elayer/CreditCardClusteringProject/blob/main/dendrogram.png "Dendrogram")

### K-Means Clustering Observations
Following the application of K-Means on the data, I could visualize how the clusters were split among the data using some attributes that differed greatly among them.
Below are a few examples of how K-Means defined the data. 

![alt text](https://github.com/elayer/CreditCardClusteringProject/blob/main/kmeans_pic1.png "KMeans Plot 1")
![alt text](https://github.com/elayer/CreditCardClusteringProject/blob/main/kmeans_pic2.png "KMeans Plot 2")

The groups are well distinguished when plotting purchases from account against account balance and purchase transactions.

## Future Improvements
I didn't use the most advanced or sophisticated clustering or pre-processing methods for this project in particular. Therefore, I wonder if applying and trying other
clustering methods such as DBSCAN or utilizing the PyCaret library could reveal deeper patterns I may not have noticed in my analysis.
