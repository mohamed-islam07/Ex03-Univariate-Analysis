# Ex03-Univariate-Analysis


# Aim
To read the given data and perform the univariate analysis with different types of plots.
 
# Explanation
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
    
# Algorithm

## Step1
Read the given data.
    
## Step2
Get the information about the data.
    
## Step3
Remove the null values from the data.

## Step4
Mention the datatypes from the data.
    
## Step5
Count the values from the data.
    
## Step6
Do plots like boxplots,countplot,distribution plot,histogram plot.
    
# Program
~~~
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/SuperStore.csv")
df
df.info()
df.isnull().sum()
df['Postal Code']=d['Postal Code'].fillna(d['Postal Code'].mode()[0])
df.head()
df.boxplot()
df['Ship Mode'].value_counts()
df['Segment'].value_counts()
df['City'].value_counts()
df['State'].value_counts()
df['Region'].value_counts()
df['Category'].value_counts()
df['Sub-Category'].value_counts()
df_count = df.groupby(by=["Category"]).count()
df_sum = df.groupby(by=["Category"]).sum()
labels=[]
for i in df_count.index:
    labels.append(i)
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
myexplode = [0, 0.2,0]
plt.pie(df_count["Sales"], colors = colors,explode = myexplode, labels=labels, autopct = "%0.0f%%",shadow = True) 
plt.show()
~~~


# Output
## Dataset
![image](https://user-images.githubusercontent.com/66360846/192726294-c1bf9a74-1488-4a69-b5a8-c5da9329a5ad.png)

## DATA INFO
![image](https://user-images.githubusercontent.com/66360846/192726553-ce33a743-a581-4f9e-8113-34e18da8bd17.png)

## DATA NULL
![image](https://user-images.githubusercontent.com/66360846/192726747-06c99d67-47fc-4368-bf70-efc464339429.png)

## APPLYING MODE TO CLEAN THE DATA
![image](https://user-images.githubusercontent.com/66360846/192726987-e727db60-a092-447a-85e1-19dc63a83688.png)

## BOX-PLOT
![image](https://user-images.githubusercontent.com/66360846/192727446-fd91f78a-080b-4419-a55c-5464e6fbe494.png)
 
## UNIVARIATE - CATEGORY
![image](https://user-images.githubusercontent.com/66360846/192727597-42c9df90-38d7-45ee-be32-8945f71b3731.png)

# Result
Thus we have read the given data and performed the univariate analysis with different types of plots.
