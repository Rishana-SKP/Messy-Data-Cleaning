# Messy-Data-Cleaning

# Data Cleaning Process

This document provides a detailed overview of the steps taken to clean the messy dataset, including assumptions made and methodologies used. This process ensures that the data is accurate, consistent, and ready for analysis.

## Steps Taken to Clean the Data

### 1. Load the Data
- **Assumption**: The CSV file is correctly formatted and accessible.
- The dataset is loaded from the CSV file using pandas.

### 2. Inspect the Data:
- Examine the data to understand its structure and identify the types of errors
and inconsistencies present.

### 3. Drop Unnecessary Column
- **Reason**: The 'Unnamed: 0' column is an artifact from saving and not needed for analysis.
- The unnecessary column is dropped from the dataset.

### 4. Handle Missing Values
- **Strategy**:
  - For `Age` and `Salary`, use the median values.
  - For `Department` and `Join Date`, use placeholders ('Unknown' for department and mode for join date).
 
### 5.Removing Duplicates:
- Identifying and removing duplicate rows to ensure each record is unique.


### 6. Correct the Email Column
- **Assumption**: Valid emails contain "@" and a domain. Invalid emails will be corrected if possible.
- **Method**: Ensure emails contain "@" and a domain. Attempt to correct invalid emails.

### 7. Filter Professional Emails
- **Assumption**: Professional emails end with common corporate domains (.com, .org, .net, .biz, .info).
- **Method**: Ensure that only professional emails are retained.

### 8. Clean the Name Column
- **Assumption**: Names should only contain alphabetic characters and spaces.
- **Method**: Remove non-alphabetic characters at the end of the name and ensure proper capitalization.

### 9. Standardize the Join Date Column
- **Assumption**: Dates should follow the format YYYY-MM-DD.
- **Method**: Convert the 'Join Date' column to datetime format and ensure consistent formatting.

### 10. Clean the Department Column
- **Assumption**: Department names should contain only standard names.
- **Method**:  Use regular expression to standardized department names.


### 11. Handle Salary Noise
- **Strategy**: Define outliers using IQR method and cap salaries outside this range.

### 12. Save Cleaned Data
- The cleaned dataset is saved to a new CSV file.

## Conclusion:
The above steps ensure that the data is clean, consistent, and ready for further analysis. Each step addresses specific issues found in the dataset, from correcting invalid email formats to standardizing department names and handling salary noise.
