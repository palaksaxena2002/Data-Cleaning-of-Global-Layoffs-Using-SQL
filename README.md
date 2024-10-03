# Data-Cleaning-of-Global-Layoffs-Using-SQL
The aim of this project is to clean and standardize a dataset containing layoff information from various companies. The project involves removing duplicates, handling null values, formatting data, and performing other data cleansing tasks to ensure data consistency and readiness for analysis.

### Key Features:
1. **Creation of Staging Table**: 
   - A copy of the original dataset is created in a staging table to preserve raw data during cleaning operations.
   
2. **Duplicate Removal**:
   - Identification and deletion of duplicate records using `ROW_NUMBER()` with `PARTITION BY`.
   - Checked for specific duplicates, such as for companies "Oda" and "Casper."

3. **Data Formatting and Standardization**:
   - Trimming whitespace from the company names using `TRIM()`.
   - Updating incorrect values in the `industry` column (e.g., replacing a URL with 'Newspaper').
   - Formatting the `date` column and altering its datatype to `DATE`.

4. **Null and Blank Values Handling**:
   - Identification of null or blank values in `total_laid_off` and `percentage_laid_off` columns.
   - Deletion of rows with both columns as blank or null.

5. **Data Type Corrections**:
   - Modified columns like `date` and `funds_raised` to appropriate data types.

6. **Data Quality Checks**:
   - Performed checks on `industry`, `location`, `stage`, `country`, and other columns to identify inconsistencies and rectify them.

### Technologies Used:
- **SQL**: Data cleaning and transformation using MySQL.
- **CTE (Common Table Expressions)**: For identifying and deleting duplicates.
- **Window Functions**: Usage of `ROW_NUMBER()` to handle duplicates.
- **String Functions**: `TRIM()` to clean up textual data.
- **Date Functions**: `STR_TO_DATE()` to reformat and standardize date values.

### Result/Impact:
- The cleaned dataset is consistent, free from duplicates, and has properly formatted data, making it ready for further analysis or reporting. This ensures that any insights derived from the data are based on accurate and reliable information, improving decision-making around company layoffs.

