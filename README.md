
# Food Nutrition Clustering
### [Colab Link](https://colab.research.google.com/drive/1zuSKOjEMKTToJR3iCNQClwbgFyjug4jL)

### Objective
In this notebook, I aim to analyze the nutrition information of different products, and perform k-means clustering based on nutrition ingredients. In the end, foods are segmented into four clusters and dietary recommendations are proposed based on nutrition.

### Modeling
#### 1.  Clustering

**Choose Number of Clusters**  Looks from the Yellowbrick Visualizer Elbow Method with below two criteria, 2 or 4 clusters is ideal.
- **silhouette**: mean ratio of intra-cluster and nearest-cluster distance.
The score is bounded between -1 for incorrect clustering and **+1 for highly dense clustering**. Scores around zero indicate overlapping clusters. The score is higher when clusters are dense and well separated, which relates to a standard concept of a cluster.
- **calinski_harabaz**: ratio of within to between cluster dispersion.
**The score is higher** when clusters are dense and well separated, which relates to a standard concept of a cluster. The score is fast to compute.

#### 2.  PCA

Looks from variance plot, three PCA is ideal, and they can be interpreted as follows:
- PC1: high carbohydrates, high sugar, and high energy, which is very common in pasta and rice, hence can be interpreted as staple food;
- PC2: high fat, high protein, and high energy, which is very common in nuts
- PC3: high fat, high sugar, and low carbohydrates, which is very common in fried food like burger and chips, hence can be interpreted as junk food;

#### 3.  Cluster Interpretation

From the visualization based on PCA, we can see that there are four clear clusters. With the nutrition characteristic and word cloud for each cluster, we can interpret them as follows:
- Cluster 0： vegetables and fruits
- Cluster 1： pasta, rice and oatmeal
- Cluster 2： nuts
- Cluster 3： snacks and junk food
![image1](/images/Picutre1.png)


### Recommendation for Consumers
Vegetables and fruits are low in sugar and fat, which is healthy and recommended for everyone.
Pasta, rice and oatmeal provides energy for human body but some of them are sugar-heavy, hence products in this group are not recommended for people with diabetes or obesity.
Nuts is high in both fat and protein, while there is no need to worry about the heavy fat because it’s healthy and beneficial to angiocarpy.
The last category snacks and junk food contains much fat and sugar, which is the least healthy food for human, hence we should be careful not to over-consume.

![image2](/images/Picutre2.png)
