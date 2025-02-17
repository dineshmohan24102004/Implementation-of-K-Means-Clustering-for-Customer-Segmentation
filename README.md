# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import standard libraries in python for finding Implementation-of-K-Means-Clustering-for-Customer-Segmentation.
2. Initialize and print the Data.head(),data.info(),data.isnull().sum()
3. Import sklearn.cluster import KMeans
4. calculate the value of KMeans Clusters.
  5. plot the graph from Elbow method and find y_pred values .
6. plot the graph from Customer Segments Graph.


## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Dinesh.M
RegisterNumber: 212222040039

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1).csv")
print("data.head():")
data.head()
print("data.info():")
data.info()
print("data.isnull().sum():")
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range (1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
print("Elbow Method Graph:")
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

print("KMeans cluster value:")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

print("y_pred:")
y_pred = km.predict(data.iloc[:,3:])
y_pred

print("Customer Segments Graph:")
data["cluster"] = y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="yellow",label="cluster4")
plt.legend()
plt.title("Customer Segments")


*/
```

## Output:
## data.head()
![image](https://github.com/dineshmohan24102004/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119478475/bafa164d-581e-438e-8cb9-1eaa02368fd7)
## data.info()
![image](https://github.com/dineshmohan24102004/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119478475/db93ff6e-0df0-4e39-95da-1644ee02bdca)

![image](https://github.com/dineshmohan24102004/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119478475/623a5727-6b3c-4e2a-aec3-3d21a19b966c)
![image](https://github.com/dineshmohan24102004/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119478475/d20586b9-b10c-4d73-9cc8-866e2fb4cd82)






## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
