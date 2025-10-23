# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.
# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.
# Algorithm:
STEP 1:Include the necessary Library.
STEP 2:Read the given Data.
STEP 3:Apply data visualization techniques to identify the patterns of the data.
STEP 4:Apply the various data visualization tools wherever necessary.
STEP 5:Include Necessary parameters in each functions.
# Coding:
~~~

import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,5,1,7,1]
sns.lineplot(x=x,y=y)
df=sns.load_dataset("tips")
df
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='dashed',legend="auto")
avg_total_bill=df.groupby('day')["total_bill"].mean()
avg_tip=df.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="total bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="tip")
plt.xlabel('day of the week')
plt.ylabel("amount")
plt.title("average total bill and tip by day")
plt.legend()
sns.barplot(x='day',y='total_bill',hue="sex",data=df,palette="Set2")
plt.xlabel("daya of the week")
plt.ylabel("total bill")
plt.title("total bill by day and gender")
import pandas as pd
t=pd.read_csv("/content/titanic_dataset (1).csv")
t
plt.figure(figsize=(8,5))
sns.barplot(x="Embarked",y="Fare",data=t,palette="Set1")
plt.title("fare of passenger by embarked town")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df)
plt.xlabel("total bill")
plt.ylabel("tip amount")
plt.title("scatterplot of total bill vs tip amount")
import numpy as np
np.random.seed(1)
num_v=np.random.randn(1000)
num_v=pd.Series(num_v,name="Numerical Variable")
num_v
sns.histplot(data=num_v,kde=True)
sns.boxplot(x=df['day'],y=df['total_bill'],hue=df['sex'])
sns.boxplot(x='day',y='total_bill',hue='smoker',data=df,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
sns.violinplot(x='day',y='total_bill',hue="smoker",data=df,linewidth=2,width=0.6,palette='Set3',inner="quartile")
plt.xlabel("day of the week")
plt.ylabel("total bill")
plt.title("violin plot of total bill by day and smoker status")
sns.set(style='whitegrid')
sns.violinplot(x="day",y='tip',data=df)
sns.set(style='whitegrid')
sns.violinplot(x=df["total_bill"])
sns.kdeplot(data=df,x="total_bill",hue="time",multiple='fill',linewidth=3,palette="Set2",alpha=0.8)
sns.kdeplot(data=df,x="total_bill",hue="time",multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
~~~
# Output:
 ![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/19ac9ab5-8134-4cc1-b858-257cb134a3a6)
![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/4d4c9be9-a0e3-45e0-9dd2-121c3de0acb2)
![327994060-e986993b-b696-447b-ab75-bde185b2e9ca](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/3f9c8900-b684-4baa-962a-25774e92d680)
![327994048-4b5ba758-c8ac-47f5-ba4a-15d3139a8e1e](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/b3aae934-301c-4ffc-b4e2-84ed949d3236)
![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/bd6fa810-b2b7-44e2-acd0-f3421470032b)
![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/86079e26-f976-4565-a3bb-3a7f55c0420c)
![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/1ad4389a-dd0a-4bfe-8211-6c25846d154f)
![image](https://github.com/RakshithaK11/EXNO-6-DS/assets/139336455/7275e58e-b90c-4d34-b70e-4262724da3d6)
# Result:
Thus to perform data visualiation using seaborn python library is successfully executed using given datas.

