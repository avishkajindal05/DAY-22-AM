Q1 — What is the difference between loc and iloc in Pandas?
>
The main difference is how they reference data:
loc is label-based. You use the actual names of the row indices or column headers. It is inclusive of the stop boundary (e.g., 0:2 includes index 2).
iloc is integer-based. You use the numerical position (0, 1, 2...). It follows standard Python slicing, so it is exclusive of the stop boundary (e.g., 0:2 excludes index 2). 

Q2 (Coding) — Write code to:
● Filter rows where a column value is greater than average
>
import pandas as pd
filtered_df = df[df['score'] > df['score'].mean()]

Q3 — What is the purpose of describe()? What insights can we get from it?
>
The describe() method provides a statistical summary of your DataFrame. It’s used to quickly understand the distribution and "shape" of your data without looking at every row. 
Insights you get:
Central Tendency: The mean (average) and 50% (median).
Dispersion: std (standard deviation) tells you how spread out the values are.
Range: min and max values.
Outliers: Comparing the max to the 75% percentile can help you spot potential outliers.
Data Integrity: The count helps you identify missing values immediately.