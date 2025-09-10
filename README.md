This notebook demonstrates the process and impact of feature scaling on machine learning models using the Social_Network_Ads.csv dataset. The primary goal is to predict whether a user will purchase a product (Purchased) based on their Age and EstimatedSalary.

The notebook is divided into two main parts:

Part 1: Effect of Scaling on Model Performance

Data Preparation:

Loads the dataset and selects the 'Age', 'EstimatedSalary', and 'Purchased' columns.

Splits the data into a 70% training set and a 30% testing set.

Feature Scaling:

Applies StandardScaler to the training data to standardize the features. StandardScaler transforms the data to have a mean of 0 and a standard deviation of 1.

The same scaler is then used to transform the test data.

Visualization:

It uses scatter plots and Kernel Density Estimate (KDE) plots to visually compare the distribution of the 'Age' and 'EstimatedSalary' features before and after applying StandardScaler. The plots show that while the shape of the distributions remains the same, their scale and center are adjusted to be comparable.

Model Comparison:

Logistic Regression: Two models are trained—one on the original data and one on the scaled data. The accuracy scores are compared, showing that for this model, scaling had a minimal negative effect (Actual: 87.5% vs. Scaled: 86.6%).

Decision Tree Classifier: The same comparison is done for a Decision Tree. In this case, scaling slightly improved the performance (Actual: 86.6% vs. Scaled: 87.5%). This highlights that the impact of feature scaling is algorithm-dependent.

Part 2: Investigating the Effect of Outliers

Introducing Outliers:

Three new data points with extreme values for Age and EstimatedSalary (e.g., age 5 with salary 1000, and ages 90/95 with salaries 250,000/350,000) are intentionally added to the dataset to simulate outliers.

Re-evaluation Setup:

The notebook then re-splits the data and re-applies the StandardScaler.

A final scatter plot visualizes how these new outliers affect the data distribution before and after scaling, setting the stage for analyzing how scaling handles data with extreme values.
