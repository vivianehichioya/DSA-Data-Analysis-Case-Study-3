# **DSA-Data Analysis Case Study 3**
The dataset used for this project is from Palmoria Group, a manufacturing company based in Nigeria. PowerBi was used to analyse the dataset and generate insights that the Palmoria management team would need to address.

## **About the Dataset**
- Two datasets were used:
  - Pulmoria Group emp-data containing employee data
    - Total Fields: 6 columns
    - Total Records: 1015 rows
  - Palmoria Group Bonus Rules containing the bonus per department per rating.
    - Total fields: 6 columns
    - Total Records: 12 rows.

## **Exploratory Data Analysis (EDA)**
- **Transformation of the first dataset**
  - Replaced value - to assign a Generic gender (male) to blank cells in the Gender column.
  - Filtered rows - To delete blanks in the salary column.
  - Replaced value and filtered rows - to replace null in the Department column with blanks and then delete empty rows.
  - Conditional column - Used to group the salary of employees into bands of 10 e.g. $21K-$30K
  - After transformation:
    - Total Fields: 7 columns
    - Total Records: 946 rows
- **Transformation of the Second Dataset**
  - Unpivot columns- to arrange the bonus rules dataset to prepare it for merging.
  - After transformatiom:
    - Total Fields: 3 columns
    - Total Records: 60 rows
- **Merge** - to extract the rating column from the bonus rules dataset data to add to the Pulmoria Group Dataset. Two common columns (Department and Rating) were selected in each of the datasets. Inner join was used to match the rows.
  - after merging:
    - Total Fields: 10 columns
    - Total Records: 875 rows
  - The reduction in the number of rows is because some employees were not rated. Those not rated were not matched.
- **Calculations**
  - DAX was used for the calculations.
  - Amount paid to individual employees: Custom column was added and named to "Bonus Payments".
    - Formula: Salary*Bonus Value
  - Total amount paid to individual employees: Custom column was added and named "Total Salary".
    - Formula: Salary+Bonus Payments
   
## **Visualisation of Results**
