![image](https://github.com/user-attachments/assets/76c79a42-58a9-4407-a1a0-54f5610e116f)# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
import seaborn as sns
import matplotlib.pyplot as plt
```
```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/bc1c8ba5-63c4-4503-877e-0c014c5139d1)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend=)
```
![image](https://github.com/user-attachments/assets/ed20f9d8-1a50-4be7-9111-a4c8e1e07861)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/10226424-6f8b-40e9-8a1a-3b11dadf6b37)
```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Amount Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/c3f99147-0dd5-4d04-b65a-52dd2745a266)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/06881a42-0fb4-4c8b-ac9b-63d2a74bbc63)
```
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/44f41ae3-57a9-436c-990d-099659305492)
```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![image](https://github.com/user-attachments/assets/20f4a433-9026-408e-a67e-4db5aa335ae7)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/510ac6ab-0c61-4e65-86a6-4e7fdd40434f)
```
sns.boxplot(x='day',y='total_bill',hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"red","edgecolor":"yellow"},
whiskerprops={"color":"green","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image](https://github.com/user-attachments/assets/99d522f7-a705-4066-bb78-8129ba828f7f)

```
df=sns.load_dataset("tips")
```
```
import seaborn as sns

import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/34565028-f1a1-474a-968f-fe10822a1bc9)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![image](https://github.com/user-attachments/assets/982feece-a59a-4256-b1be-5480889cd47f)
```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/1ebfcde1-3ed2-45ea-b31c-1a5d90506a16)
```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/57f7629b-f7d3-4487-ae7b-7c706507e4fe)
```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set2', alpha=0.8)
```
![image](https://github.com/user-attachments/assets/b216d059-44d4-4cd2-9cb6-705c3e68da41)
```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)
```
![image](https://github.com/user-attachments/assets/872f5af4-0d8d-40ba-a3ef-6e3b255e530c)
```
hms=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/692ee956-7405-4d91-b71e-4c7522358937)
```
hms=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/93d59758-f724-49e4-96a1-d6f41eab4102)
```
import numpy as np
df=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(df)
```
![image](https://github.com/user-attachments/assets/a3ff0a99-dec6-4b9b-9b24-d668d62b1af1)
```
hms=sns.heatmap(data=df)
```
![image](https://github.com/user-attachments/assets/67aec223-955b-45e9-9139-11977fb5cecf)
```
hms=sns.heatmap(data=df,annot=True)
```
![image](https://github.com/user-attachments/assets/05770b59-a94a-4d2c-8ba0-2c7c55e0031f)
```
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
```
```
sns.heatmap(corr,annot=True,cmap="plasma",linewidths=0.5)
```
![image](https://github.com/user-attachments/assets/62ba9f31-bb6a-4d43-bc75-5417de675057)


# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
