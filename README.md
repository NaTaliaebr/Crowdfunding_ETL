For the ETL mini project, you will work with a partner to practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you?ll upload the CSV file data into a Postgres database.
Since this is a one-week project, make sure that you have done at least half of your project before the third day of class to stay on track.
Although you and your partner will divide the work, it?s essential to collaborate and communicate while working on different parts of the project. Be sure to check in with your partner regularly and offer support.
Files
Download the starter code and files to help you get started:
Project 2 ETL files
Before You Begin
1. Create a new repository, named?Crowdfunding_ETL, for this project.?Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Rename the?ETL_Mini_Project_Starter_Code.ipynb?file with your first name initial and last name, for example,?ETL_Mini_Project_NRomanoff.ipynb. Then, add this Jupyter notebook file and the Resources folder containing the?crowdfunding.xlsx?and the?contacts.xlsx?files to your repository.
4. Push the changes to GitHub
Instructions
The instructions for this mini project are divided into the following subsections:
* Create the Category and Subcategory DataFrames
* Create the Campaign DataFrame
* Create the Contacts DataFrame
* Create the Crowdfunding Database
Create the Category and Subcategory DataFrames
1. Extract and transform the?crowdfunding.xlsx?Excel data to create a category DataFrame that has the following columns:
o A "category_id" column that has entries going sequentially from "cat1" to "catn", where?n?is the number of unique categories
o A "category" column that contains only the category titles
o The following image shows this category DataFrame:

2. Export the category DataFrame as?category.csv?and save it to your GitHub repository.
3. Extract and transform the?crowdfunding.xlsx?Excel data to create a subcategory DataFrame that has the following columns:
o A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where?n?is the number of unique subcategories
o A "subcategory" column that contains only the subcategory titles
o The following image shows this subcategory DataFrame:

4. Export the subcategory DataFrame as?subcategory.csv?and save it to your GitHub repository.
Create the Campaign DataFrame
1. Extract and transform the?crowdfunding.xlsx?Excel data to create a campaign DataFrame has the following columns:
o The "cf_id" column
o The "contact_id" column
o The "company_name" column
o The "blurb" column, renamed to "description"
o The "goal" column, converted to the?float?data type
o The "pledged" column, converted to the?float?data type
o The "outcome" column
o The "backers_count" column
o The "country" column
o The "currency" column
o The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the?datetime?format
o The "deadline" column, renamed to "end_date" and with the UTC times converted to the?datetime?format
o The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
o The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
o The following image shows this campaign DataFrame:

2. Export the campaign DataFrame as?campaign.csv?and save it to your GitHub repository.
Create the Contacts DataFrame
1. Choose one of the following two options for extracting and transforming the data from the?contacts.xlsx?Excel data:
o Option 1:?Use Python dictionary methods.
o Option 2:?Use regular expressions.
2. If you chose Option 1, complete the following steps:
o Import the?contacts.xlsx?file into a DataFrame.
o Iterate through the DataFrame, converting each row to a dictionary.
o Iterate through each dictionary, doing the following:
* Extract the dictionary values from the keys by using a Python list comprehension.
* Add the values for each row to a new list.
o Create a new DataFrame that contains the extracted data.
o Split each "name" column value into a first and last name, and place each in a new column.
o Clean and export the DataFrame as?contacts.csv?and save it to your GitHub repository.
3. If you chose Option 2, complete the following steps:
o Import the?contacts.xlsx?file into a DataFrame.
o Extract the "contact_id", "name", and "email" columns by using regular expressions.
o Create a new DataFrame with the extracted data.
o Convert the "contact_id" column to the integer type.
o Split each "name" column value into a first and a last name, and place each in a new column.
o Clean and then export the DataFrame as?contacts.csv?and save it to your GitHub repository.
4. Check that your final DataFrame resembles the one in the following image:

Create the Crowdfunding Database
1. Inspect the four CSV files, and then sketch an ERD of the tables by using?QuickDBD.
2. Use the information from the ERD to create a table schema for each CSV file.
Note:?Remember to specify the data types, primary keys, foreign keys, and other constraints.
3. Save the database schema as a Postgres file named?crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named?crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a?SELECT?statement for each table.
7. Import each CSV file into its corresponding SQL table.
8. Verify that each table has the correct data by running a?SELECT?statement for each.

