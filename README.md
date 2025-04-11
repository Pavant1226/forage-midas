# Midas
Project repo for the JPMC Advanced Software Engineering Forage program
import pandas as pd
import matplotlib.pyplot as plt

# Load the CSV data
df = pd.read_csv('data.csv')

# Convert Date to datetime
df['Date'] = pd.to_datetime(df['Date'])

# Plot the closing prices
plt.plot(df['Date'], df['Close'], marker='o')
plt.title('Stock Price Over Time')
plt.xlabel('Date')
plt.ylabel('Close Price')
plt.grid(True)
plt.show()
