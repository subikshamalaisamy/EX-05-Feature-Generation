# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE

import pandas as pd

df=pd.read_csv('/content/Encoding Data.csv')

df.head()

df['ord_2'].unique()

from sklearn.preprocessing import LabelEncoder, OrdinalEncoder

climate = ['Cold', 'Warm', 'Hot']

en= OrdinalEncoder(categories = [climate])

df['ord_2']=en.fit_transform(df[["ord_2"]])

df

le = LabelEncoder()

df['Nom_0'] = le.fit_transform(df[["nom_0"]])

df

!pip install --upgrade category_encoders

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data = be.fit_transform(df['bin_1'])

df = pd.concat([df,data],axis=1)

df

be= BinaryEncoder()

data = be.fit_transform(df['bin_2'])

df = pd.concat([df,data],axis=1)

df

df1 = pd.read_csv("/content/data.csv")

df1.head()

df1['Ord_1'].unique()

climate = ['Cold', 'Warm', 'Hot', 'Very Hot']

en= OrdinalEncoder(categories = [climate])

df1['Ord_1']=en.fit_transform(df1 [["Ord_1"]])

df1

df1['Ord_2'].unique()

cl= ['High School', 'Diploma', 'Bachelors', 'Masters', 'PhD']

en= OrdinalEncoder(categories = [cl])

df1['Ord_2']=en.fit_transform(df1 [["Ord_2"]])

df1

le = LabelEncoder()

df1['City']= le.fit_transform(df1[["City"]])

df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data1 = be.fit_transform(df1['bin_2'])

df1 = pd.concat([df1,data1],axis=1)

df1

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df2 = pd.concat([df2,data2],axis=1)

df2

df2 = pd.get_dummies (df2, prefix=["Embarked"],columns=['Embarked'])

df2

# OUPUT
<img width="254" alt="image" src="https://user-images.githubusercontent.com/87276633/233913779-e317e78a-63ad-4786-845e-c969a88d61b1.png">
<img width="344" alt="image" src="https://user-images.githubusercontent.com/87276633/233913892-55f680d7-8ef7-4932-abdd-d157b1be367b.png">
<img width="361" alt="image" src="https://user-images.githubusercontent.com/87276633/233914018-249d2d5c-2b8a-4b8c-8e41-393b75a7afe9.png">
<img width="407" alt="image" src="https://user-images.githubusercontent.com/87276633/233914196-65395c0c-05fb-49f8-a887-2a0c67ce180a.png">
<img width="470" alt="image" src="https://user-images.githubusercontent.com/87276633/233914146-614eea7c-fdff-470c-8959-7788271983f9.png">
<img width="382" alt="image" src="https://user-images.githubusercontent.com/87276633/233914253-d83ada63-1611-4a53-b9bb-f5bb89219ed4.png">
<img width="358" alt="image" src="https://user-images.githubusercontent.com/87276633/233914297-ccd471ce-9361-44b6-aa2a-24692579a67d.png">
<img width="411" alt="image" src="https://user-images.githubusercontent.com/87276633/233914510-68d5293d-3900-4d9b-b37c-020753c96fa9.png">

