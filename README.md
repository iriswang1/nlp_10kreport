# Text Mining 10-K Filing Report to Predict Financial Distress Using Risk Factors


### Overview
Using natural language processing and machine learning to predict financial distress from Risk Factors section in 10K filling annual report

### Motivation
One of the most critical issues facing financial institutes such as banks is to measure ability of the clients to repay loans. In another words, the financial distress, which indicates a probability a company goes to bankruptcy (the client cannot repay loans), is an important indicators to many financial institutes as well as companies themselves.

### Introduction
The financial institutes use Moody’s edf score to measure financial distress, which calculated by numerical data. Financial distress can be unveiled from several warning signs of company’s financial performance, such as poor profits, negative cash flow, declining relationship with the bank, etc. The “Risk Factor Section” in the 10-K annual report  includes company’s explanation of the risks it faces, which contains information regarding future firm fundamentals that is not captured by the quantitative information.

### Objective
Improve financial distress (edf) prediction based on risk factors in 10-K filing report from 2012 to 2016.

### Project Pipeline
- Data prepration: 
   - The crucial and huge data source are full 10-K documents in plain text for 19027 companies for range 1 to 30 years separately. All 10-K documents are saved in a folder under different subfolders named with a unique key referred to the company with specific paths. The unique key which every company has is called 'gvkey'. The 'gvkey' is the key to connect 10-K reports and other data sources. 
   - The second part is a sas7bdat file named KMV.sas7bdat, which includes ‘gvkey’, ‘datadate’, ‘edf’ and other columns. I processed the KMV file and only kept 'DATE' (transferred from datadate, and was only kept the year), 'gvkey' and 'edf' for further propose.
   - The third data source is a CSV file named sec_index_complete.csv, which contains ‘gvkey’, ‘Actual 10K Path Raw’ and other variables. ‘Actual 10K Path Raw’ points to the actual locations of the 10-K documents. I merged the 'Actural 10K Path Raw' with KMV file by 'gvkey'.
   -  The Actual 10K Path Raw can help to link to the raw 10-K reports. I scraped the Risk Factor Section by using Regular Expression. Below text shows a partial content of a typical text of Risk Factor Section in a company’s filing report.
- Text mining (NLP)
- Prediction Modeling


