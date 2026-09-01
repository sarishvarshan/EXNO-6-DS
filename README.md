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

# Coding and Output:

````
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()

````


<img width="1418" height="256" alt="image" src="https://github.com/user-attachments/assets/ea975299-7d5b-46dd-983a-64ac905b8d1f" />



````
#LINE PLOT:
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

````

<img width="686" height="578" alt="image" src="https://github.com/user-attachments/assets/71cbf5ed-1571-4294-ae3f-b29035248ccf" />


````

#MULTI LINE PLOT:
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')

````

<img width="717" height="583" alt="image" src="https://github.com/user-attachments/assets/b3a6da75-e149-4765-aefa-71e7cbdfb130" />



````

#BAR CHART:
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

````

<img width="900" height="605" alt="image" src="https://github.com/user-attachments/assets/f51c113a-5d02-4b7f-b12c-3f9acb5cd64b" />


````
#SCATTER PLOT:
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

````

<img width="752" height="578" alt="image" src="https://github.com/user-attachments/assets/12a834d3-6996-48dd-89de-57fd072ce236" />



````
#BUBBLE CHART:
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

````

<img width="743" height="577" alt="image" src="https://github.com/user-attachments/assets/c83c02da-b702-482a-8f89-0ca16185d6ed" />


````

#HISTOGRAM:
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

````

<img width="757" height="573" alt="image" src="https://github.com/user-attachments/assets/7bf9be0f-a50c-4bd9-ad6f-8e03dab38f5d" />


````

#BOX PLOT:
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
````

<img width="766" height="620" alt="image" src="https://github.com/user-attachments/assets/808597e7-3358-4360-b839-2de788ff6d09" />


````

#VIOLIN PLOT:
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

````

<img width="768" height="572" alt="image" src="https://github.com/user-attachments/assets/d1a00cd5-1263-423e-998f-6a51b2ddeba7" />

````

#DESTINY PLOT:
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
````
<img width="741" height="600" alt="image" src="https://github.com/user-attachments/assets/9b20e305-637b-4a9e-9622-af746397d71c" />

```
#HEATMAP:
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```
<img width="828" height="645" alt="image" src="https://github.com/user-attachments/assets/06244812-a160-49ae-89f2-63e3cabab1d8" />






# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
