# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE
```
NAVEENAA V.R
212221220035
```
```
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_csv("/content/Superstore - Superstore.csv (1).csv")
df.head()
df.info()
df.isnull().sum()
LINE PLOT
sns.lineplot(x="Category",y="Sales",data=df,marker='o')

sns.lineplot(x='Ship Mode', y='Category',hue="Segment",data=df)
plt.title("Multiline Plot")
plt.show()
BAR PLOT
sns.barplot(x="Category",y="Sales",data=df)

sns.barplot(x='Region', y='Sales', data=df,palette='Set1')
plt.title("Sales in different Regions")
plt.show()
SCATTER PLOT
sns.scatterplot(x='Category',y='Sub-Category',data=df)
plt.title("Scatterplot")
plt.show()

sns.scatterplot(x='Category',y='Sub-Category',hue='Segment',data=df)
plt.show()
BOX PLOT
sns.boxplot(x="Sub-Category",y="Discount",data=df)
plt.xticks(rotation=90)

sns.boxplot( x="Profit", y="Category",data=df)
POINT PLOT
sns.pointplot(x=df["Quantity"],y=df["Discount"])
VIOLIN PLOT
sns.violinplot(x="Profit",data=df)
COUNT PLOT
sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)
plt.xticks(rotation=90)
HISTOGRAM
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
KDE PLOT
sns.kdeplot(x="Discount", data = df,hue='Category')
Data Visualization using Matplotlib
PLOT
plt.plot(df['Region'], df['Sales'])
plt.show()
HEATMAP
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
PIE CHART
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
BAR PLOT
plt.bar(df['Category'],df.index)
plt.show()
SCATTER PLOT
plt.scatter(df["Region"],df["Profit"], c ="red")
plt.show()
BOX PLOT
plt.boxplot(x="Sales",data=df)
plt.show()
```
## OUTPUT
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/7e258d7a-d4a2-4077-ae3f-32b8afff6d72)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/4dc70649-b919-4698-b37a-10d2bd5bbd0e)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/7a6f79bb-6b16-4613-bf5b-65866e5e43cb)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/5514ad7e-2a91-4b4e-a9cc-83938ca3c0f6)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/7021724f-8ab5-43eb-9cb5-13cb80f038e9)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/a4bd8599-9162-4f92-818e-28e4d91b2461)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/cb527cdc-3d2f-4919-98b5-b311c0ab0924)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/13b674e6-70d5-405e-afa7-20e81890f820)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/7e3429ed-b04f-4b88-93dd-26546397077b)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/c3c9d9d5-74d1-4e64-8887-eb4569c8db2f)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/ef4dd176-0db7-4c60-a525-d81030300f01)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/c60895d9-65ce-49a1-8458-3099d888e526)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/d140d0e9-2b37-4fb4-8cd1-f1a7efb1dabd)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/f1e20fea-2bf7-437c-9de3-39d457faf185)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/26141b40-c67c-466d-abce-58a890af57cb)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/980d0452-0a25-49bd-bd7a-60c07a382370)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-08/assets/131433133/9cd46859-c0a4-456f-ae75-d4bc91feb118)
## RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.


