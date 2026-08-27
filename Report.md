# E-Commerce Data Analysis Report

# Project Overview

This project focuses on cleaning, validating, analyzing, and visualizing an e-commerce dataset using Python.

The main objective of the project is to improve the quality of the dataset and perform Exploratory Data Analysis (EDA) to understand customer behavior, sales patterns, product categories, payment methods, and other important relationships in the data.

---

# 1. Dataset Description

### Original Dataset

`messy_ecommerce_15000_student_practice.csv`

The dataset contains e-commerce order information. It includes both numerical and categorical data.

### Important Columns

| Column | Description |
|---|---|
| Age | Age of the customer |
| Gender | Gender of the customer |
| City | Customer's city |
| Product_Category | Category of the purchased product |
| Unit_Price | Price of one product unit |
| Quantity | Number of products purchased |
| Discount | Discount applied to the order |
| Payment_Method | Method used for payment |
| Rating | Customer rating |
| Delivery_Days | Number of days taken for delivery |
| Returned | Return status of the order |
| Total_Amount | Final order amount |

The dataset was analyzed using:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

# 2.  Data Quality Problems Identified

The dataset was checked carefully to identify possible data-quality problems.

The following issues were investigated:

### Missing Values

Some columns contained missing or empty values. Each column was analyzed separately before selecting an appropriate method to handle the missing data.

### Inconsistent Categorical Values

Categorical columns were checked for different representations of the same value.

Examples include differences in:

- Uppercase and lowercase letters
- Extra spaces
- Different formats of the same category

These inconsistencies can create incorrect category counts during analysis.

### Duplicate Records

The dataset was checked for:

- Exact duplicate rows
- Duplicate `Order_ID` values

Duplicate records can affect statistical calculations and produce incorrect results.

### Possible Outliers

Numerical columns were analyzed to identify unusually high or low values.

The following columns were included in the outlier analysis:

- Age
- Unit_Price
- Quantity
- Discount
- Rating
- Delivery_Days
- Total_Amount

### Data Consistency

The `Total_Amount` column was validated by comparing it with the expected order amount calculated from the available order-related values.

---

# 3.  Data Cleaning Techniques Used

Several data-cleaning techniques were applied to improve the quality of the dataset.

### Handling Missing Values

Missing values were handled based on the type and nature of each column.

Possible methods included:

- Mean
- Median
- Mode

The entire dataset was not simply dropped because removing all rows with missing values could result in unnecessary data loss.

### Standardizing Categorical Data

Inconsistent categorical values were standardized into a common format.

This helped ensure that the same category was not counted multiple times because of differences in capitalization or formatting.

### Removing Duplicate Records

Exact duplicate rows were identified and removed from the dataset.

The dataset was checked again after removal to confirm that the duplicate records had been handled correctly.

### Outlier Investigation

Outliers were detected using:

- Seaborn boxplots
- IQR method

Not every outlier was automatically removed. Each unusual value was treated carefully because an outlier can be a valid extreme value and not necessarily an error.

### Data Validation

The dataset was checked again after cleaning to verify:

- Dataset dimensions
- Data types
- Missing values
- Duplicate records
- Unique values
- Categorical consistency
- Outliers
- Data consistency

---

# 4.  Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the dataset through different visualizations.

## 4.1 Univariate Analysis

The following visualizations were created to study individual variables:

- Histogram of `Age`
- Histogram of `Total_Amount`
- KDE plot of `Unit_Price`
- Boxplot of `Total_Amount`
- Countplot of `Product_Category`
- Countplot of `Payment_Method`
- Countplot of `Gender`

These plots helped in understanding the distribution, frequency, spread, and possible unusual values in the dataset.

---

## 4.2 Bivariate Analysis

Relationships between two variables were analyzed using different Seaborn visualizations.

The following comparisons were performed:

- Age vs Total_Amount
- Unit_Price vs Total_Amount
- Discount vs Total_Amount
- Product_Category vs Total_Amount
- Gender vs Total_Amount
- Payment_Method vs Total_Amount

Appropriate plots such as bar plots, scatter plots, boxplots, and violin plots were used based on the type of variables.

---

## 4.3 Multivariate Analysis

Multivariate analysis was performed to understand relationships among multiple variables.

The following techniques were used:

- Pairplot for selected numerical variables
- Correlation heatmap
- Categorical comparisons using hue

Examples of categorical comparisons include:

- Product_Category and Gender
- Product_Category and Returned
- Payment_Method and Returned

---

# 5.  Correlation Analysis

A correlation matrix was created for the numerical columns.

The correlation analysis was used to identify:

1. Strong positive relationships
2. Strong negative relationships
3. Weak relationships
4. Variables that may be useful for understanding `Total_Amount`

The heatmap made it easier to visually understand how numerical variables are related to each other.

Order-related variables such as `Unit_Price` and `Quantity` are especially important when analyzing `Total_Amount` because they are directly connected to the value of an order.

---

# 6.  Important Observations

Some important observations were made during the analysis:

- The dataset contained different types of numerical and categorical variables.
- Data cleaning was necessary before performing reliable analysis.
- Missing values required different treatment depending on the column.
- Inconsistent categorical values could affect category counts and visualizations.
- Duplicate records could affect statistical results if they were not removed.
- Some numerical columns contained possible outliers.
- Outliers were investigated instead of being automatically removed.
- Visualizations helped in understanding the distribution and relationships between variables.
- Correlation analysis helped identify variables related to `Total_Amount`.

> **Note:** The final observations should always be based on the actual output generated in the Jupyter Notebook.

---

# 7.  Business Insights

The analysis was used to answer important e-commerce business questions.

### Product Analysis

- Which product category receives the most orders?
- Which category has the highest average order value?
- Which categories have better customer ratings?

### Customer Analysis

- Which city generates higher sales?
- Is there a difference in average spending between gender categories?
- What patterns can be observed from customer age?

### Payment Analysis

- Which payment method is used most frequently?
- Does payment method show any difference in order amount?

### Discount Analysis

- Does discount appear to influence the total order amount?
- How does the order value change across different discount values?

### Return Analysis

- What percentage of orders are returned?
- Are some product categories associated with more returned orders?
- Is there any visible pattern between payment method and returned orders?

### Delivery and Rating Analysis

- Does delivery time appear to have any relationship with customer ratings?
- Do longer delivery times show different customer satisfaction patterns?

---

# 8.  Final Cleaned Dataset

After completing the data-cleaning process, the cleaned dataset was saved separately as:

`cleaned_ecommerce_dataset.csv`

The original dataset was kept unchanged.

### Data Cleaning Process

```text
messy_ecommerce_15000_student_practice.csv
                    │
                    ▼
             Data Cleaning
                    │
                    ▼
       cleaned_ecommerce_dataset.csv

9. Final Conclusion
This project successfully performed data cleaning, data validation, and exploratory data analysis on an e-commerce dataset.

The dataset was examined for missing values, inconsistent categorical data, duplicate records, possible outliers, and data consistency problems. Appropriate cleaning techniques were applied, and the results were verified after the cleaning process.

Different types of visualizations were created using Matplotlib and Seaborn. Univariate, bivariate, multivariate, and correlation analysis helped in understanding the dataset from different perspectives.

The project also explored useful business questions related to products, customers, payments, returns, discounts, delivery, ratings, and order amounts.