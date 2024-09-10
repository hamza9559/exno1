# Exno:1
# Data Cleaning Process
# NAME: HAMZA FAROOQUE
# REG.NO: 212223040054
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
1.Read and Display Dataframe
```
import pandas as pd
df= pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![Screenshot 2024-09-10 103422](https://github.com/user-attachments/assets/8638504e-1de5-463d-8eea-03851f26009e)

2.Display Head
```
df.head(5)
```
![Screenshot 2024-09-10 111119](https://github.com/user-attachments/assets/427aa214-dcd4-4355-885e-186b162aa040)

3.Display Tail
```
df.tail(5)
```
![image](https://github.com/user-attachments/assets/6a8c711d-ed76-452f-af5d-e005ff608826)

4.Info of DataFrame
```
df.info()
```
![image](https://github.com/user-attachments/assets/910b9275-f7e1-4d21-9fd2-f03b894bae49)

5.Describe about Dataframe
```
df.describe()
```
![image](https://github.com/user-attachments/assets/638281c9-aee3-4d1b-a5c7-ce65e33872c0)

6.Shape of the dataframe
```
df.shape
OUTPUT: (21, 12)
```

7.Checking the NUll values
```
df.isnull().sum()
```
![image](https://github.com/user-attachments/assets/d048dec7-b085-4b3b-a094-4165d0a8f985)

8.Drop the Null values in Total
```
df.TOTAL.fillna(mn, inplace=True)
df
```
![image](https://github.com/user-attachments/assets/e9f3a999-1be1-499a-a754-faac4bc37381)

9.Determinig the Duplicates
```
df.duplicated()
```
![image](https://github.com/user-attachments/assets/f87f81b9-4bd8-4227-9afd-020e638968be)

10.Deleting the duplicates
```
df.drop_duplicates(inplace=True)
df
```
![image](https://github.com/user-attachments/assets/07f76752-05e8-4df9-bb91-5a948e564b6d)

11.Highlighting Null values
```
import seaborn as sns
sns.heatmap(df.isnull(), yticklabels=False, annot=True)
```
![image](https://github.com/user-attachments/assets/19b9f0c7-924b-40cb-833f-908446a39fac)

12. After dropping null values
```
import seaborn as sns
sns.heatmap(df.isnull(), yticklabels=False, annot=True)
```
![image](https://github.com/user-attachments/assets/b704c356-6621-4ac5-a9ce-be06bd09f9e3)

# Result 
Thus the data cleaning process has been successfully completed. 
