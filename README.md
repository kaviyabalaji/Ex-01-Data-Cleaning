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
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/1.png)
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/2.png)
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/3.png)
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/4.png)
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/5.png)
![o](https://github.com/kaviyabalaji/Ex-01-Data-Cleaning/blob/main/6.png)
![o](
# Result
Hence the given data is read and perform data cleaning and save the cleaned data to a file.
