# Real-Estate-Analysis

- The following code is a data cleaning report for the "Bengaluru_House_Data.csv" file. The data cleaning process involves several steps such as data preprocessing, feature engineering, and outlier removal.

## Data Preprocessing:
The first step in the data cleaning process is to drop the irrelevant columns such as 'area_type', 'availability', 'society', and 'balcony'.
The next step is to check and remove any missing values in the data. The code uses the .isnull().sum() method to check for missing values in the data and .dropna() to remove them.
The code then converts the size column into a numerical format by extracting the number of bedrooms (bhk) and creating a new column 'bhk'.
The code also handles the range values in the 'total_sqft' column. A custom function convert_sqrt_to_num is created to convert range values into an average of the two values.
## Feature Engineering:
A new column 'Price_per_sqft' is created to calculate the price per square feet of the property.
The code then reduces the number of unique values in the 'location' column. The locations with less than 10 properties are grouped into 'other'. This is done to reduce the size of the 'location' column for one-hot encoding.
## Outlier Removal:
The code removes the outliers by using business logic. The outlier is considered to be any property with a 'total_sqft' to 'bhk' ratio less than 300 square feet per bedroom. This is considered unusual, and such properties are removed.

- `Overall`, the data cleaning process ensures that the data is free of missing values, range values, and outliers. The feature engineering step creates new features that can help in further analysis.
