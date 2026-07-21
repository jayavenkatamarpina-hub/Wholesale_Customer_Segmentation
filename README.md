# Wholesale Customer Segmentation — K-Means vs DBSCAN

Segmenting wholesale customers by annual spending across 6 product categories (Fresh, Milk, Grocery, Frozen, Detergents_Paper, Delicassen), comparing two clustering approaches.

## What's in this notebook

- Scaled the 6 spending features with StandardScaler
- Used the elbow method to pick k=5 for K-Means
- Applied K-Means and DBSCAN to the same scaled data
- Reduced the data to 2D with PCA (72.5% of variance retained) for visualization
- Scatter plots comparing cluster assignments from both algorithms
- Compared average spending per cluster to interpret what each group represents

## Result

K-Means split customers into 5 groups, ranging from typical low-spending buyers to a single extreme outlier account. DBSCAN took a simpler approach, grouping most customers (393) into one dense "typical" cluster while flagging 47 unusually high-spending customers as noise rather than forcing them into subgroups. Both algorithms agree on the core insight: most customers behave similarly, while a meaningful minority are distinct, high-volume buyers.

## Files

- `Wholesale_Customer_Segmentation.ipynb` - the notebook
- `Wholesale customers data.csv` - the dataset
