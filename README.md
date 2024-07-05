# Visitor Sum by Weekday

This script calculates the total number of visitors for each weekday from a given dataset using Pandas.

## Sample Output

```python

import pandas as pd
import numpy as np

# Given data
d = [
    {'city': 'Austin', 'visitor': 139, 'weekday': 'Sun'},
    {'city': 'Dallas', 'visitor': 237, 'weekday': 'Sun'},
    {'city': 'Austin', 'visitor': 326, 'weekday': 'Mon'},
    {'city': 'Dallas', 'visitor': 456, 'weekday': 'Mon'}
]

# Create DataFrame
df = pd.DataFrame(d)

# Group by 'weekday' and calculate the sum of 'visitor'
visitor_sum = df.groupby('weekday')['visitor'].sum()

# Convert the result to dictionary format
result = visitor_sum.to_dict()

# Output the result
print(result)
