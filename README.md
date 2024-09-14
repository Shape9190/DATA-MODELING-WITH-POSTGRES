# DATA MODELING WITH POSTGRES 

## Overview:
> A music streaming startup called Sparkify is looking to better understand how customers use thier app. They have collected significant data but the data has not been organized or used as a resource up to this point. They have asked for assistance in creating a data schema for them so they can begin optimizing thier data and better understand the songs popular with thier customers. 

## Objective:
> In addition to creating a clear relational database for Sparkify to conduct their queries, I also created an ETL pipeline. The ETL pipeline allows for files from seperate data directories combine data into a single accessable directory for ease of analysis. The ETL also allwos for seperate analysis to be cunducted and then compared. 

## The Data:
> The data was orignially in two JSON files and had information regarding songs played on the app. The info ranged from "artisit_id" to "registration_number". There had been no orginaization or formating to normalize these datasets. 

> After reviewing the datasets, I decided to use a star schema for this project. Since there is only need for one fact table(songplays), the rest of the tables will be sectioned off to tables of relevance and joined by the fact table which will hold all of the primary keys. 
I created 5 seperate data tables: "songsplayed","users","songs","artists",and "time".

## Repository:
> Within the repository there are 6 files/folders:
    * data.zip - Song and Log data in JSON format
    * create_tables.py - Activates Create and Drop of tables
    * sql_queries.py - SQL queries and ETL 
    * etl.ipynb - converts a song_data and log_data into the tables
    * etl.py - converts all song_data and log_data into the tables
    * test.ipynb - where database tables are queried for insights
    
## How to Run the Scripts
> 1. create tables:
    * create_tables.py
> 2. insert data to tables via ETL
    * ely.py
> 3. view data:
    * test.ipynb
> 4. reset: 
    * creates_tables
> 5. rerun steps 1-4

## Takeaway:
> Sparkify now has a functioning data model that contains clear individualized tables containing only relevant data per table. Datasets that were once congested and difficult to navigate are now organized to for Sparkify to use as an insight of users and song trends.