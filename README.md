# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
Program developed by: KIRUTHIKA S

Register number: 212221040085
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# OUPUT
# DATA
![image](https://user-images.githubusercontent.com/128348968/229421885-e356c150-2849-4d6a-be2d-b21a97318216.png)
# NON NULL BEFORE
# df.info
![image](https://user-images.githubusercontent.com/128348968/229422248-a47dc6a5-9243-45f8-b09b-e5747e101e28.png)
# Mode
![image](https://user-images.githubusercontent.com/128348968/229422307-22bef788-6d53-48f6-9d5b-7328316bbe5b.png)
# Mean
![image](https://user-images.githubusercontent.com/128348968/229422439-933654ad-745b-4f55-8d18-9870e29a67e0.png)
# Median
![image](https://user-images.githubusercontent.com/128348968/229422597-fc38f698-34fa-41e8-98ef-a26baf01bd44.png)
# NON NULL AFTER
# df.info()

# df.isnull().sum()

#Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
