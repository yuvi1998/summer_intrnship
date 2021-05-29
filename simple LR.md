import pandas
ds = pandas.read_csv('Salary_Data.csv')
ds.columns
x = ds['YearsExperience'].values.reshape(-1,1) 
y = ds['Salary']
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(x , y)
import joblib
joblib.dump(model , 'salery.pk1')
