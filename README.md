# SQL

#### # The dataset:
<a href="https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results">120 years of Olympic history</a>
#### # DBMS:
I am using <a href="https://www.postgresql.org/download/">PostgreSQL</a>. For interface: pgAdmin. If you want to use something else, download your favourite one.
#### # Loading data into PostgreSQL:
Extract the data. We will get two file and the data will be in CSV format. So, we have to import the data into our database. The step to follow:
<p><b>Step 1:</b> Create a database named olympic or any of your choice.</p>
<p><b>Step 2:</b> As, the downloaded dataset contains two file.. so, we need to create two table to load the data. For creating table wither we can create table manually of simply can use query. I have used query to create table. Here is the query:</p>

<p>CREATE TABLE IF NOT EXISTS OLYMPICS_HISTORY (</p>
    <p>id          INT,</p>
    <p>name        VARCHAR,</p>
    <p>sex         VARCHAR,</p>
    <p>age         VARCHAR,</p>
    <p>height      VARCHAR,</p>
    <p>weight      VARCHAR,</p>
    <p>team        VARCHAR,</p>
    <p>noc         VARCHAR,</p>
    <p>games       VARCHAR,</p>
    <p>year        INT,</p>
    <p>season      VARCHAR,</p>
    <p>city        VARCHAR,</p>
    <p>sport       VARCHAR,</p>
    <p>event       VARCHAR,</p>
    <p>medal       VARCHAR</p>
<p>);</p>

<p>CREATE TABLE IF NOT EXISTS OLYMPICS_HISTORY_NOC_REGIONS (</p>
    <p>noc         VARCHAR,</p>
    <p>region      VARCHAR,</p>
    <p>notes       VARCHAR</p>
<p>);</p>

<p><b>Step 3: Import the data</b> </p>
<p>To import the data, right click on the table where we want to load data and choose Import/Export. Choose the file, file extension, set headers on, and set escape to "". As we have double quoted data or simply modify the data manually.</p>
<p><b>Step 4:</b> It's done. Check if the data has loaded correctly or not: select * from OLYMPICS_HISTORY;
select * from OLYMPICS_HISTORY_NOC_REGIONS;</p>
