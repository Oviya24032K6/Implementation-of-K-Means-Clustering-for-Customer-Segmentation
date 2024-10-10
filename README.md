# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplot libraries.
2.import Kmeans algorithm to solve customer segmentation.
3.Using the for loop cluster the given data
4.Predict the output and plot data graphs.
5.Display the outputs

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: OVIYA P 
RegisterNumber:  212223110033
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
kmeans=KMeans(n_clusters=i,init="k-means++")
kmeans.fit(data.iloc[:,3:])
wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No_of_Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segment")
```

## Output:
1.DATA.HEAD():
![image](https://github.com/user-attachments/assets/3433a877-d83d-476b-96bf-8aa5677aeeee)
2.DATA.INFO():
![image](https://github.com/user-attachments/assets/c0ba6e3d-a6d6-4617-888a-6023e5823f94)
3.DATA.ISNULL().SUM():
![image](https://github.com/user-attachments/assets/de451ad9-546b-42e6-aea5-a38803dec047)
4.PLOT USING ELBOW METHOD:
![image](https://github.com/user-attachments/assets/d9425ed9-6531-4288-9a28-b9207c366520)
5.K-MEANS CLUSTERING:
![image](https://github.com/user-attachments/assets/5faa1bff-e06f-4de4-a218-94834b5e266b)
6.Y-PRED ARRAY:
![image](https://github.com/user-attachments/assets/294ee8c5-b824-4387-80d6-bcf249a77e1a)
7.CUSTOMER SEGMENT:
![image](https://github.com/user-attachments/assets/73d86761-8251-40da-b261-b2c34ce93d85)


## Result:

Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
