#### DEND Project 1B

# Data Modeling with Apache Cassandra

### Summary of the project

In this project we performed analyses for startup Sparkify.
To accomplish this task we used NoSQL database Apache Cassandra. Data modeling was performed based on queries, which were planed to run. Sparkify

### Data

Data were shared in CSV  files and located in directory __\event_data__

### Process

1. First we gathered all log files under one file
2. Limited records for analytics purposes
3. Created Keyspace "Sparkify"
4. Created tables in accordance with sample CQL queries:

Query1:
> 'SELECT * FROM music_app_history WHERE sessionId=338 AND itemInSession=4'

Query2:
> 'SELECT * FROM user_songs_in_session WHERE userid = 10 AND sessionid = 182'

Query3:
> "SELECT user_fname, user_lname FROM users_listened_this_song WHERE song_title ='All Hands Against His Own'"

![tables](/images/all_tables.png "CQL tables design")

### Setting environment

To run project locally you need Apache Cassandra Database and Python installed. You can find appropriate package and installation guides here:

- <a href="http://cassandra.apache.org/doc/latest/getting_started/installing.html">Apache Cassandra</a>
- <a href="https://www.anaconda.com/distribution/">Anaconda for Python</a>

We also going to need two libraries installed for our script - **Pandas** (to be able to read CSV file into dataframe object and perform operations on it) and **Cassandra** Python driver (to interact with database).

To instal Pandas, run in Terminal:
> conda install pandas

To install Cassandra:
> pip install Cassandra

### How to run
You can Notebook file in the directory:

* Project_1B_ Project_Template.ipynb

To open this file, navigate to this directory via Terminal(Shell/Command line) and run command:
> jupyter notebook

This command lunches Jupyter notebook in your browser. Now you are able to see your directory via notebook, click on file __Project_1B_ Project_Template.ipynb__. Run each cell with CTRL+RETURN
