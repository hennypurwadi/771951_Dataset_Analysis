This dataset is a collection of global retail company in United States, shows the transaction details from a retail operation, linking customers, orders, and products through sales records. It includes:
Customer information ('Customer ID', 'Customer Name', 'Segment','Country', 'City', 'State', 'Postal Code', 'Region'),

Order specifics ('Order ID', 'Order Date', 'Ship Date', 'Ship Mode'), where 'Order Date' and 'Ship Date' are incorrectly categorized and should be in Datetime format.

Product attributes ('Product ID', 'Category', 'Sub-Category', 'Product Name'),

Sales transactions ('Sales', 'Quantity', 'Discount', 'Profit'), which should be in Numeric format.

There are some challenges which need to be addressed before analysis can be conducted. Among these challenges are missing values, typos, also errors that are scattered around the datas. Missing values can impact the accuracy of any analysis, leading to incorrect conclusions.

Typos, particularly in text-based fields such as 'Product Name' or 'Customer Name', create inconsistencies which complicate categorization and analysis.

Errors, which manifest as incorrect entries in numerical fields like 'Sales', 'Quantity', 'Discount', 'Profit', or inaccuracies in 'Order Date' and 'Ship Date' fields, can mislead analysis then affect the reliability of any insights from the dataset.

Addressing these issues is very important to ensure the integrity of the analysis, requiring a data cleaning process to identify these imperfections, to enhance the dataset's quality and reliability for analytical tasks.

Before analysis can commence, need to clean the dataset to be prepared due to several issues. Begins with importing necessary libraries such as pandas, NumPy, matplotlib, and seaborn. The initial step involves loading a dataset, followed by preliminary cleaning. This includes handling missing values, correcting data types like converting 'Order Date' and 'Ship Date' to datetime format, and addressing inconsistencies/ errors in the data, such as typos in several columns.

Inconsistencies are everywhere, with notable typos in 'Order Date' and 'Ship Date' columns leading to unrealistic delivery periods, such as 91 days. Furthermore, the date fields are not formatted as datetime, and the 'Quantity' and 'Profit' columns, which should be numerical, are erroneously listed as object data types. This situation complicates any attempts to correct data types without first addressing the missing values.

The initial phase involves segregating dataset (df) into 4 groups: df_Product, df_Sales, df_Customer, and df_Order, and then cleaning each group individually. This stage covers rectifying missing information, adjusting data types, and later merging these cleaned segments into a unified dataset (df1).

Tackle missing values:
Apply imputation techniques, filling in gaps with correspondence values from similar data. This step is necessary for the integrity of our dataset.

Correcting date entries is another critical task. Incorrect placements of day and month values can lead to skewed delivery times; therefore, adjustments—such as swapping the day and month—are made to ensure that delivery schedules accurately mirror reality.

After rectifying these preliminary issues, we compile the cleansed data into a comprehensive dataset ready for further analysis.

Outlier Detection and Removal:
Using statistical methods like the calculation of z-scores, identifies outliers within the dataset is necessary, especially in numerical columns such as 'Sales', 'Quantity', 'Discount', 'Profit'. These outliers are removed to normalize the data distribution and improve the accuracy.

Normalization or Scaling:
To ensure uniformity in the dataset, especially before conducting any form of multivariate analysis, apply scaling techniques to numerical variables. This process ensures that variables are on a similar scale, preventing any one variable from disproportionately influencing the analysis.

Descriptive Statistical Analysis:
After cleaning, performs a descriptive statistical analysis to summarize the central tendencies, dispersion, and shape of the dataset's distributions. This include calculating means, medians, modes, variances, and standard deviations for numerical data, providing a solid understanding of dataset's characteristics.

Univariate Analysis:
The univariate analysis focusing on single variables to understand the individual properties.

Visualization:
Various data visualizations are to convey findings effectively. This could range from simple line plots and bar charts to more complex visualizations like heatmaps for correlation matrices, or pie charts to illustrate proportional relationships.
