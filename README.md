# ADS-Assignment-2-3

#import employee-Attrition data csv file

import pandas as pd

import matplotlib.pyplot as plt

hr_data = pd.read_csv("./WA_Fn-UseC_-HR-Employee-Attrition.csv")

df = pd.DataFrame(data = hr_data).dropna()
#df = df.dropna(inplace = True)
df = df.drop_duplicates()

df.head()

df.describe().head()

df.columns


df_1 = ['DistanceFromHome','JobRole', 'Attrition']

df_1 = df[df_1]

df_1



df_2 = ['MonthlyIncome','Education', 'Attrition', 'Age']

df_2 = df[df_2]
df_2

import matplotlib.pyplot as plt

ax = plt.gca()

df_2.plot(kind = 'scatter', x ='Age', y ='MonthlyIncome', ax = ax )

plt.show

df_2.groupby('Education') ['MonthlyIncome'].nunique().plot(kind = 'bar')

plt.show





















