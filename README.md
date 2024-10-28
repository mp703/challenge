# Mindex Data Analytics Code Challenge

## Prerequisites
- Python 3.x
- DBeaver

## Setup Instructions
- `pip install -r requirements.txt`
- Run code blocks in `mindex_data_analytics_code_challenge.ipynb`
- Connect to PostgreSQL DB and run the following SQL Query:

   ```sql
   SELECT 
       SUM("Boyd_Yards") AS "Boyd Yards",
       SUM("Chase_Yards") AS "Chase Yards",
       SUM("Higgins_Yards") AS "Higgins Yards",
       CONCAT(
           COUNT(CASE WHEN "Result" = 'Win' THEN 1 END), 
           ' - ', 
           COUNT(CASE WHEN "Result" = 'Loss' THEN 1 END)
       ) AS "Win/Loss"
   FROM michael_paquette;
