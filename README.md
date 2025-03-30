
# Banking Risk Analytics Report

## Problem Statement

This project aims to develop a fundamental understanding of risk analytics in banking and financial services. The goal is to understand how data is utilized to minimize the risk of financial loss while lending to customers.

## Solution

We utilize Power BI dashboards to facilitate decision-making based on applicant profiles. The dashboards help determine whether to approve a loan based on the likelihood of repayment.

## Dataset Overview

The dataset includes information about bank details and various client profiles, structured in multiple interlinked tables using primary and foreign keys. Key tables include:

- Banking Relationship
- Client-Banking
- Gender
- Investment Advisor
- Period

## Data Cleaning

- **Income Band Creation**: 
  - Estimated Income < 100,000 is categorized as "Low"
  - Estimated Income < 300,000 is categorized as "Mid"
  
- **Processing Fees Column**: 
  - A new column is created to define processing fees based on the fee structure.

## Calculated Functions

### Common Functions

- **Sum**: 
  - Syntax: `Sum = SUM(<column>)`
  - Example: `Bank Deposit = SUM('Clients - Banking'[Bank Deposits])`

- **DistinctCount**: 
  - Syntax: `DISTINCTCOUNT(<column>)`
  - Example: `Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID])`

- **Sumx**: 
  - Syntax: `SUMX(<table>, <expression>)`
  - Example: `Total Fees = SUMX('Clients - Banking', [Total Loan] * 'Clients - Banking'[Processing Fees])`

- **Switch**: 
  - Syntax: `SWITCH(<expression>, <value>, <result>[, <value>, <result>]…[, <else>])`

- **DATEDIFF**: 
  - Syntax: `DATEDIFF(<Date1>, <Date2>, <Interval>)`
  - Example: `Engagement Days = DATEDIFF('Clients - Banking'[Joined Bank], TODAY(), DAY)`

## Key Performance Indicators (KPIs)

- **Total Clients**: Represents the total number of clients in banking.
- **Total Loan**: Information about bank loans, business lending, and credit card balances.
- **Total Fees**: Total amount charged by the bank for various services.

## Visualization and Results

Dashboards include:

- Home
- Loan Analysis
- Deposit Analysis
- Summary Dashboard

## Conclusion

Power BI dashboards are powerful tools in the banking sector, providing valuable insights into key banking metrics and KPIs.

## Future Work

Future enhancements include:

- Analyzing total loan amounts and client distributions across different banks.
- Identifying trends related to client demographics and their banking preferences.
- Providing insights into various account types and the amounts involved.

## Getting Started

1. Clone the repository.
2. Ensure you have Power BI installed.
3. Open the .pbix file to view the dashboards.
4. Modify the dataset as needed for your analysis.



## Screenshots

![Screenshot 2025-03-30 202107](https://github.com/user-attachments/assets/eb5e34cd-c6ac-457e-9e9a-b7ed430d2091)


![Screenshot 2025-03-30 202118](https://github.com/user-attachments/assets/0d464104-ddfe-419b-809d-0c98b575c135)


![Screenshot 2025-03-30 202126](https://github.com/user-attachments/assets/24c128c0-0973-440f-af20-ccd1384cfbaa)


![Screenshot 2025-03-30 202137](https://github.com/user-attachments/assets/343d9a61-f2ee-4e37-ac23-667985639a77)
