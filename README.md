# Music Streaming Application

Under this project, I have created this ETL pipeline for a hypothetical startup called Sparkify. Sparkify wants to analyze the data which they have collected on songs and user activity for thier new music streaming service. All of this data sits in a directory of JSON logs of user activity, as well as a directory with JSON metadata on the songs in their app.

My role in this project as a Data Engineer is to create a Postgres database with the tables designed to optimize queries on song play analysis. I also have created the database schemas and the ETL pipeline for the analysis. 

## Project Description

Creating an ETL pipeline using Python. The pipeline transfers data from files in two local local directories into the tables in Postgres using Python and SQL. This project also includes defining the fact and dimension tables for a star schema for a particulcar analytic focus.

## Datasets

The first dataset is a subset of real data from the Million Song Dataset. Each file is in JSON format and contains metadata about a song and the artist of that song.

The second dataset consists of log files in JSON format generated by an event simulator based on the songs in the dataset above.

## Database Schema for Song Play Analysis

This schema is star based schema creating one fact table and 4 dimension tables. 

Fact Table
songplays - records in log data associated with song plays

Dimension Tables
users - users in the app
songs - songs in music database
artists - artists in music database
time - timestamps of records in songplays broken down into specific units

Dimension tables makes is easy for you to update details of users and artists minimizing time and effort rather than updating in every log.

# ETL pipeline

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

## Prerequisites

What things you need to install and how to install them

python 2.7 or above

PostgreSQL database adapter for the python - psycopg2
<p><code>pip install psycopg2</code></p>

## Scripts

Run sql_queries.py (it contains all the sql queries that is needed to create and drop tables, and insert data)
<p><code> python sql_queries.py </code></p>
  
Then run create_tables.py to create schema and tables
<p><code> python create_tables.py </code></p>

and lastly run etl.py to complete the ETL process
<p><code> python etl.py </code></p>

test.ipynb can be used to check and analyze data in the database tables.
