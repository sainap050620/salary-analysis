import pandas as pd
office = {
    "Name": ["Saina","Dev","Karan","Binita","Sarosh"],
    "Salary": ["50000","40000","10000","2000","9000"],
    "Department": ["DS","DS","Bio","House","Bank"]
}

# Create a DataFrame from the dictionary
df = pd.DataFrame(office)

# Convert 'Salary' column to numeric (from string)
df['Salary'] = pd.to_numeric(df['Salary'])

# Calculate the mean of the 'Salary' column
avgS = df["Salary"].mean()
print(f"Mean Salary: {avgS}")

# Find employees with salary greater than 50000
top = df[df['Salary'] > 10000]
print("\nTop Earners (Salary > 50000):")
print(top)

# The original line topn=df.info(top) is incorrect usage.
# If you wanted info about the 'top' earners DataFrame, you would do:
# top.info()
df
