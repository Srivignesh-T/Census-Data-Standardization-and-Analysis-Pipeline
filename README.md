# Census-Data-Standardization-and-Analysis-Pipeline

## Discription :-
The Census Data Standardization and Analysis Pipeline project aims to standardize and analyze census data efficiently. 
It involves creating a pipeline that processes raw census data, performs data standardization and cleaning, conducts analysis using various data science techniques, and generates meaningful insights and visualizations.

---

## Tools Used :-
[Python](https://www.python.org/downloads/)__, [Pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html)__, [MySQL Connector Python](https://pypi.org/project/mysql-connector-python/)__, [PyMongo](https://pypi.org/project/pymongo/)__, [Streamlit](https://docs.streamlit.io/)

---

## Workflow :-
1. Load Data:
  * Load the census data from the source files into a pandas DataFrame.
2. Rename Columns: 
  * Rename specific columns to ensure uniformity in the datasets
3. Standardize State/UT Names:
  * Convert the State/UT names to a consistent format (first letter uppercase, rest lowercase, except "and")
4. Handle New State/UT Formations:
  * Update State/UT names for districts affected by the formation of Telangana (2014) and Ladakh (2019) using provided district lists.
5. Find and Process Missing Data:
  * Calculate and fill missing data using logical relationships between columns.
  * Compare and store the percentage of missing data before and after filling
6. Fetch and Upload Data to Relational Database:
  * Store the processed data in a MongoDB collection named “census”.
7. Run Queries and Display output in Streamlit:
  *Execute queries to retrieve specific insights from the relational database (e.g., total population, literacy rates).
  * Display the results of the queries on a Streamlit web application for easy visualization and analysis.
  * 
>[!NOTE]
1 - 6 were done in the 'census data cleansing.ipynb' file.
The Streamlit is a seperate file named as 'census_streamlit.py'

### Requirements Installation
  // Install the required packages
  pip install -r requirements.txt
  
### Execute Command:

  // To run census_streamlit.py file
  streamlit run census_streamlit.py

***

>[!WARNING]
1. Kindly make sure that the required packages are installed.
2. Please make sure you're connect to your MongoDB and MySQL server before running these files.
3. Please run the census data cleansing.ipynb file first, because file consists the Data imports, cleaning and uploading to Database.
4. Kindly makesure that you've installed Streamlit before running the census_streamlit.py file, if not then open the terminal and execute the command - 'pip install streamlit'
5. In order to run the census_streamlit.py , open the command prompt and use the above 'execute command'
