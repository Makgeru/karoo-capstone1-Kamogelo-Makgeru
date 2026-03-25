# karoo-capstone1-Kamogelo-Makgeru

📄 Design & Implementation Overview
Database Design

I was initially provided with three tables. Based on the project requirements, I extended the schema by creating two additional tables and refining the structure for better normalization and relationships.

One key change was made to the target table, which I renamed to sales_target. I added a region_id column to improve consistency and enable proper relationships.

In the suppliers table, the original design attempted to connect using a region field. Since this field was not unique, I replaced it with a region_id foreign key to ensure referential integrity. I also added two additional columns to the suppliers table to support the overall data model.

The suppliers table serves as a central (normalizing) table connecting other parts of the database.

Relationships

The relationships in the database are as follows:

Suppliers ↔ Certifications: Many-to-Many
Suppliers ↔ Harvest: Many-to-Many
Orders → Suppliers: One-to-Many
Sales_target → Suppliers: Many-to-One
Automation & Data Loading

For the automation component, I used a Jupyter Notebook environment.

The process included:

Setting up the environment and required dependencies
Loading the SQL extension
Importing necessary libraries such as pandas
Creating a database connection using create_engine from sqlalchemy

I then created tables corresponding to the initial dataset to prepare them for insertion into the database.

During the data loading process, I automated the insertion of data into the database. After creating the additional tables, I ensured all data was properly structured and inserted.

Analytics

Once the data was successfully loaded, I executed analytical SQL queries to extract insights from the database.

⚙️ Summary

This project involved:

Extending and normalizing an existing schema
Improving relationships using foreign keys
Automating data loading using Python and SQLAlchemy
Running analytical queries on the final dataset