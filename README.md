### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 22/04/2025
### AIM: 
To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```
# Visitor segmentation based on characteristics
import pandas as pd
import matplotlib.pyplot as plt

# Read the data
df = pd.read_csv('/content/clustervisitor.csv')

# Define age groups
age_groups = {
    'Young ': (df['Age'] <= 30) ,
    'Middle': (df['Age'] >= 31) & (df['Age'] <= 60),
    'Old': (df['Age'] > 61)
}

# Count visitors in each age group
visitor_counts = []
for group in age_groups:
    count = df[age_groups[group]].shape[0]
    visitor_counts.append(count)
```
### Output:

### Visualization:
```
# Plotting
age_group_labels = list(age_groups.keys())

plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:

![image](https://github.com/user-attachments/assets/947e4ee4-aa75-4795-8d2e-314ba4bc4ec5)

### Result:
Hence Cluster and Visitor Segmentation for Navigation patterns in Python is implemented.
