Download Link: https://assignmentchef.com/product/solved-sql-assignment-1-liquidity-task
<br>



The task is to calculate the liquidity ratio, which allows us to understand much better whetherthe ads are popular among seekers.Based on this, i have prepared an analysis using the available data

**Technical part:**1. SQL queries that allow for liquidity calculation.2. Preparation also in Python for calculating liquidity for all users, i.e. we want to get a list with information about exactly how much liquidity is for each user

**Analytical part:**1. Please prepare a complete analysis of the data that was sent, along with the answers to the following questions

a. What differences do you see between the segments in terms of the data you have available (including liquidity)?b. What do you think may affect the higher or lower liquidity level?

**Form:**1. Jupyter / R Markdown preferred for analysis2. The scripts can be in separate files or as part of the notebook depending on the methods chosen3. Please present the final results and the most important conclusions in the form of a presentation (e.g. Google slides)

**How to calculate the liquidity:**Liquidity is understood as the % of ads that received at least 1 response (by phone or e-mail) within 7 days.

***Example:*** &lt;/br&gt;On April 1, the user added 10 ads to the website &lt;/br&gt;From 1 to 7 April, he received responses to 6 ads. &lt;/br&gt;On April 2, another 5 ads were added and he received replies to all of them within 7 days of their appearance on the site &lt;/br&gt;

The **liquidity calculation** is (6 + 5) / (10 + 5) = 73%

## DatasetThe data we have at our disposal:

1. Data_ads (date, user_id, ad_id, category_id, params) – here you can find information about ads2. Data_replies (date, user_id, ad_id, mails, phones) – information about replies to the ads on a given day3. Data_categories (category_id, category_name) – mapping to a category tree4. Data_segments (user_id, segment) – mapping to segmentation for each user

## Analysis

&lt;br/&gt;

**Scope**

The task is to calculate the liquidity ratio, which allows us to understand much better whether the ads are popular among seekers.

**Calculation**

Liquiddity calculation can be found here : https://github.com/nmafb/Liquidity/blob/main/notebooks/Data_Analysis.ipynb

**Analysis**

Complete analysis can be found here : https://docs.google.com/presentation/d/188Mfq4VgL4YS5VDK4RZBTOD0o8QxekCwROT7et4gwUY/edit#slide=id.p

&lt;br/&gt;

## Project repository structureThe following folders and files are contained in the project repository:

“`.liquidity|│ README.md # Project description and documentation│ .gitignore # Files and extension ignored in commited│ docker-compose.yml # Container for postgres and pgadmin│ requirements.txt│└───data # Locally data source (csv files)│ └───raw│ │ │ data_ads.csv│ │ │ data_replies.csv│ │ │ data_segments.csv│ │ │ data_categories.csv│ ││ └───processed│ │ …│└───resources # Project resources (images, others…)│ │ …│└───notebooks # Jupyter notebooks│ │ Data_Analysis.ipynb│ │ Data_Exploration.ipynb└───src # Source code│ └───Python # – Python code| | create_tables.py│ | | etl.py│ | | sql_queries.py| └─── SQL # – SQL code| | | liquidity.sql“`

&lt;br/&gt;

The main files:

* `Data_Analysis.ipynb` notebooks which i make the data analysis. I present some graphs.

* `Data_Exploration.ipynb` notebooks which make it possible to explore the data and present some statistical data on them. I present some graphs.

* `sql_queries.py` contains all sql queries, and it’s used (imported) in other files or scripts.

* `create_tables.py` drops and creates your tables. This file should always be executed before running the ETL scripts. The db should be cleaned.

* `etl.py` reads and processes files from data and loads them into final tables.

&lt;br/&gt;

## Requirements

The following tools and packages are necessary to run the scripts locally:

* Git* Python3* jupyter notebooks* Requirements* Docker* Docker-Compose* _PostgresSQL_* _PgAdmin_

&lt;br/&gt;