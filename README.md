# Movies-ETL
## Overview
In preparation for a hackathon, Amazing Prime needed a clean dataset to use. Britta and I worked together to Extract, Transform, and Load the data. We used both Wikipedia and Kaggle datasets that we were to extract, clean and combine them into a single dataset, and load them into a SQL database for the hackathon participants to use. This was to be accomplished using one function that takes in three files and completes the ETL process by adding the cleaned data into PosgreSQL database.
#### Resources used:
Software used: Python programming language, Pandas an open source Python library, Jupyter Notebook an open source web application to create the Python and Pandas code, PostgreSQL as the relational databse, and pgAdmin as the open source administrator for PostgreSQL

Data sources: movies_metadat.csv and rating.csv from kaggle.com and wikipedia-movies.json

## Results
After loading the files from the data sources, we wrote a function that would to put the files into dataframes, clean the data by removing bad or corrupt data, then merged the data into one file before loading it into a PostgreSQL database. The function also would take the ratings.csv file and load it in the database. The results are below:

The movie table contains the cleaned movie data merged from the movies_metadata.csv, the ratings.csv, and data from the wikipedia-movies.json
<img src=Resources\movies_table.png> This made 6,052 rows of movie data

<img src=Resources\movies_query.png>



A section of the function code loaded the rating csv file dirctly into a separate table


<img src=Resources\ratings_table.png>

This shows that there is 26,024,289 rows of ratings data

<img src=Resources\ratings_query.png>


## Summary

There were many challenges in the process, like trying to determine what data was necessary, what data could be dropped, and some bumps in the road with trying to refactor the code into a single function. In the end, we were able to create the SQL database that contains the cleaned data for the Amazing Prime Hackathon, the ETL process was a success.