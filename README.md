# Welcome to the Sparkify Project!

## Project Explanation

Sparkify has been collecting data on songs and user activity through their streaming app.  Analytics team would like to know what songs that users are listening to.

### Data
The data resides in a directory of JSON logs on user activity and a directory with JSON metadata about the songs.
### Log Dataset
Simulated user activity logs
Partitioned by year and month, ex:
> - log_data/2018/11/2018-11-12-events.json
> - log_data/2018/11/2018-11-13-events.json

#### Song Dataset
JSON metadata about songs and artists, partitioned by the first three letters of each song's track ID, ex:
> - song_data/A/B/C/TRABCEI128F424C983.json
> - song_data/A/A/B/TRAABJL12903CDCF1A.json

### Goal
Create a Postgres database with tables designed to optimize queries on song play analysis.

## Database
### Fact table:  
>songplays  
### Dimension Tables:
>users  
>songs  
>artists  
>time  
  
### Project Outline
Define fact and dimension tables in a star schema for the given analytical focus.
Write a Python ETL pipeline that transfer data from the JSON files.
Create Tables:
Write CREATE statements in sql_queries.py to create each table.
Write DROP statements in sql_queries.py to drop each table if it exists.
Run create_tables.py to create your database and tables.
Run test.ipynb to confirm the creation of your tables with the correct columns. 
Make sure to click "Restart kernel" to close the connection to the database after running this notebook
Build ETL Processes
Build ETL Pipeline
Run Sanity Tests

Document Process in this README.md:
Do the following steps in your README.md file.
    Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.
    How to run the Python scripts
    An explanation of the files in the repository
    State and justify your database schema design and ETL pipeline.
    [Optional] Provide example queries and results for song play analysis.

Provide DOCSTRING statement in each function implementation to describe what each function does.


## How to run the Python scripts
Prereqs:
- Postgres Database needs to have studentdb setup with user student and pasword student
- Data should be in json files in the data/song_data and data/log_data directories.

- First run create_tables.py - this will drop all tables if they exist and then create them again.
- Then run etl.py to extract all data from the files, transform as needed, and load into Postgres database.

## Explanation of the files in the repository
- sql_queries.py - contains all the drop, create and insert statements.  It does not need to be run but will be imported.
- create_tables.py - first drops, then creates all new tables
- etl.py - extracts all data from the files, transform as needed, and load into Postgres database

- etl.ipynb - Jupyter notebook for testing all the etl processes (run create_tables.py first, make sure you restart kernel after using to disconnect db)
- test.ipynb - Jupyter notebook for testing data integrity, runs queries on all tables and checks consistency (make sure you restart kernel after using to disconnect db)

Thanks for reading!  Rich Humphrey





