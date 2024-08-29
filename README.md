# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 29-08-24

# AIM:
To Develop a python program to Plot a time series data of XAUUSD
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
Developed By : Yohesh Kumar R.M
Reg No.      : 212222240118
```
```py
import pandas as pd
import matplotlib.pyplot as plt

file_path = '/content/Microsoft_Stock.csv'
data = pd.read_csv(file_path)

data['Date'] = pd.to_datetime(data['Date'])
data.set_index('Date', inplace=True)

plt.figure(figsize=(10, 6))
plt.plot(data['Close'], label='Close Price', color='blue')
plt.title('Time Series Plot of Microsoft Stock Prices')
plt.xlabel('Date')
plt.ylabel('Close Price')
plt.legend()
plt.grid(True)
plt.show()

```

# OUTPUT:
![download](https://github.com/user-attachments/assets/b036fe28-455b-4c34-9ee4-951e74c57d6c)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
