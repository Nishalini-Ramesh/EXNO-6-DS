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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1219" height="224" alt="image" src="https://github.com/user-attachments/assets/3aa60850-5a4b-44df-92f4-ed34938983e7" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="726" height="589" alt="image" src="https://github.com/user-attachments/assets/69f162c8-59d1-4b30-9f80-8d438e9eea98" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="691" height="589" alt="image" src="https://github.com/user-attachments/assets/29fbbb24-d259-46c2-ac01-3be7f5670d8b" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="892" height="635" alt="image" src="https://github.com/user-attachments/assets/0571e13f-b6a7-4344-9dba-2d01bf1f1a41" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/0dbaa3ce-b325-4dd6-b43a-f5eecc61287b" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/9a79b4f2-a96f-4bf9-8dcc-f32aa6c5be13" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="748" height="586" alt="image" src="https://github.com/user-attachments/assets/50ca31b7-dd10-420b-89a6-bb9043f33eec" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="750" height="606" alt="image" src="https://github.com/user-attachments/assets/cac80cf5-be25-4a15-9250-d8fa0a1113f5" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/3b3f39c6-9940-4b08-b3b9-9e46156145ff" />

```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="585" height="453" alt="image" src="https://github.com/user-attachments/assets/23c60181-2052-4cac-9357-ec0cf1be196b" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="597" height="503" alt="image" src="https://github.com/user-attachments/assets/87efd645-78b4-4af6-95a4-4278616f282b" />


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.


