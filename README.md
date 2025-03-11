# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 08.03.2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
file_path = 'DailyDelhiClimateTrain.csv'
data = pd.read_csv(file_path)
data.head()
data['date'] = pd.to_datetime(data['date'])
data.set_index('date', inplace=True)
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['meantemp'], label='DailyDelhiClimate', color='blue')

plt.title('DailyDelhiClimate')
plt.xlabel('date')
plt.ylabel('meantemp')
plt.grid(True)
plt.legend()
plt.show()

plt.figure(figsize=(10, 6))
plt.hist(data['meantemp'], bins=30, color='skyblue', edgecolor="black")
plt.title('DailyDelhiClimate')
plt.xlabel('date')
plt.ylabel('meantemp')
plt.show()

selected_columns = [ 'meantemp', 'humidity', 'wind_speed', 'meanpressure']
data[selected_columns].plot(kind='line', figsize=(15, 8))
plt.title('DailyDelhiClimate')
plt.xlabel('date')
plt.ylabel('Values')
plt.legend(loc='upper left')
plt.show()
```











# OUTPUT:
![Screenshot 2025-03-11 084837](https://github.com/user-attachments/assets/9978f781-4333-4c11-99e8-76ad2ac1c8d7)
![image](https://github.com/user-attachments/assets/0b3e9835-404c-4179-b938-b6a69dd3abdd)
![image](https://github.com/user-attachments/assets/1761202b-8a53-4ec9-8952-f96f21c28d81)
![image](https://github.com/user-attachments/assets/a59f4938-9b89-44be-8617-cd3c8998d8a7)









# RESULT:
Thus we have created the python code for plotting the time series of given data.
