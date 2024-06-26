# crowdfunding_ETL
This is an ETL mini project about building an ETL pipeline using Python, Pandas, and Python dictionary methods  to extract and transform the data. After  transforming the data, CSV files  are used  to create an ERD and a table schema and uploaded into a Postgres database.
    
## Data Source
Data for this dataset was generated by edX Boot Camps LLC. The starter files which were provided are : crowdfunding.xlsx and contacts.xlsx 

## Before you begin:
1.     A new repository, named crowdfunding_ETL was created, for this project. The new repository was cloned.
2.    The ETL_Mini_Project_JReed_AIngole.ipynb  Jupyter notebook file and the Resources folder containing the crowdfunding.xlsx and the contacts.xlsx files was added to repository.
3.    The changes were pushed to GitHub.
##Instructions:
This mini project is divided into the following  four subsections:
1.    Create the Category and Subcategory DataFrames
Data was extracted and transformed from the crowdfunding.xlsx Excel to a category DataFrame that has the following columns:
o    A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
o    A "category" column that contains only the category titles
o    The category DataFrame was exported as category.csv and saved  to GitHub repository.
Data was extracted and transformed from the crowdfunding.xlsx Excel  to create a subcategory DataFrame that has the following columns:
o    A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
o    A "subcategory" column that contains only the subcategory titles
o    The subcategory DataFrame was exported as subcategory.csv and saved to GitHub repository.

2.    Create the Campaign DataFrame
Data was extracedt and transformed from  the crowdfunding.xlsx Excel  to create a campaign DataFrame that has the following columns:
o    The "cf_id" column
o    The "contact_id" column
o    The "company_name" column
o    The "blurb" column, renamed to "description"
o    The "goal" column, converted to the float data type
o    The "pledged" column, converted to the float data type
o    The "outcome" column
o    The "backers_count" column
o    The "country" column
o    The "currency" column
o    The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
o    The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
o    The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
o    The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
o    The campaign DataFrame was exported as campaign.csv and saved to GitHub repository.

3.    Create the Contacts DataFrame
Data was extracted and transformed  from the contacts.xlsx Excel file by using Python dictionary methods :
o    The contacts.xlsx file was imported into a contact_info DataFrame.
o    The DataFrame was Iterated and converted each row to a dictionary.
o    While Iterating through each dictionary, the following was done:
    The dictionary values  was extracted from the keys by using a Python list comprehension.
    The values were added for each row to a new list.
o    A new DataFrame was created that contains the extracted data.
o    Each "name" column value was split into a first and last name, and placed in a new column.
o    The DataFrame was cleaned and exported  as contacts.csv and saved to GitHub repository.

4.    Create the Crowdfunding Database
•    With four CSV files( category.csv , subcategory.csv , campaign.csv , contacts.csv)  an ERD was sketched of the tables by using QuickDBDLinks to an external site..
•    Using the information from the ERD a table schema for each CSV file was created.
•    An image file of ERD is created and named as ERD_crowdfunding.png
•    The database schema was saved as a Postgres file named crowdfunding_db_schema.sql, and saved to  GitHub repository.
•    A new Postgres database, named crowdfunding_db was created.
•    Using the database schema, the tables were created in the correct order to handle the foreign keys.
•    The table creation was verified by running a SELECT statement for each table and saved in import_csv.sql
•    Each CSV file was imported into its corresponding SQL table.

### Prerequisites
•    Tools need to have installed before project:
•    Jupyter notebook
•    Python
•    Pandas
•    Postgresql
•    GitHub
