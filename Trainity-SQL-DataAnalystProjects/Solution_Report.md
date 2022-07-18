# Project-2: Instagram user Analytics Report.
## Project Description:
<p>In the given assignment, we must present a thorough report to Instagram's product team; the management need certain critical insights from the user schema that will be vital in driving increased user engagement for Instagram. Multiple teams will utilise the conclusions produced from the analysis for launch marketing campaigns, decide on new features for designing an app, measure the performance of the app by evaluating user engagement, and enhance the overall experience while also securing business growth.</p>
<p>The Instagram user Analytics project will focus on producing insights using SQL as the primary analytical tool. Loading the schema in the MySQL server takes the first priority.</p>

## ✍🏼 Approach:
### 1️⃣ [Creating a Database](https://github.com/Subhrajit91939/MySQL-Projects/edit/main/Trainity-SQL-DataAnalystProjects/Solution_Report.md#resources)<br>
```sql
-- Selecting the `ig_clone` database.
SHOW DATABASES;
USE ig_clone;
```
Verifying if all the tables have been created properly (or) not.

```sql
mysql> SHOW TABLES; 
+--------------------+
| Tables_in_ig_clone |
+--------------------+
| comments           |
| follows            |
| likes              |
| photo_tags         |
| photos             |
| tags               |
| users              |
+--------------------+
7 rows in set (0.02 sec)
```

### 2️⃣ The marketing team wants to launch some campaigns, and they need help with determining the following:
#### Q1. Rewarding Most Loyal Users: People who have been using the platform for the longest time.
      Task: Find the 5 oldest users of the Instagram from the database provided.
We use the `users` table to retrieve the data as it contains the users id, username and their joining date which is required for sorting the table and retrieving the 
oldest users of Instagram from the database.
```sql
SELECT
        id AS 'User-ID',
        username AS 'Username',
        created_at AS 'Joined Instagram on'
        -- Selecting the id, username and the created_at columns with proper aliasing.
FROM users
ORDER BY created_at ASC 
-- Sorting the users with respect to the created_at column using the `ORDER BY` clause in the ascending order.
LIMIT 5; -- As we need only the First 5 users for instagram, we use the `LIMIT` clause
```
```sql
mysql> source insta_task.sql
+---------+------------------+---------------------+
| User-ID | Username         | Joined Instagram on |
+---------+------------------+---------------------+
|      80 | Darby_Herzog     | 2016-05-06 00:14:21 |
|      67 | Emilio_Bernier52 | 2016-05-06 13:04:30 |
|      63 | Elenor88         | 2016-05-08 01:30:41 |
|      95 | Nicole71         | 2016-05-09 17:30:22 |
|      38 | Jordyn.Jacobson2 | 2016-05-14 07:56:26 |
+---------+------------------+---------------------+
5 rows in set (0.00 sec)
```

```sql
```

### ⚙️ Tech-Stack Used: MySQL; Code-Editor Used: VS Code
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)

## 📊📈 Insights:
Jot down the insights and the knowledge you gained while making the project. You need to write what you infer about the things. Make sure it's brief and up to the point only. For Eg. If you got a graph then what do you understand by the graph, what changes can you make or what can you derive from the graph.

## 🎯 Result:
Mention what have you achieved while making the project and how do you think it has helped you.

## 🗃️ Drive Links:
**Database:** [trainity_insta_analytics.sql](https://drive.google.com/file/d/1JwEPL15NfOepUSuV7HTINW7XEqpx0UzN/view?usp=sharing) <br>
**Project code:** [instagram_sql_analsis.pdf](https://drive.google.com/file/d/1B6KDkOkqxVYPnZhAnkqDH-Ksv7LpXx_y/view?usp=sharing) <br>
**Project code(RAW .sql file):** [insta_task.sql](https://drive.google.com/file/d/1xXbRiX4VBpCXaI5s_mS70yCqHWMSZCIU/view?usp=sharing)	<br>

## 📂 Resources:
[Instagram Project- SQL Instructions](https://docs.google.com/document/d/1-0L_ZE-RI22q8UV818BZCXL6mgKTetcbVR5PbzmAVS0/edit) <br>
[Commands for creating Database.docx](https://docs.google.com/document/d/1-WhNRX1iYJIz7e5l28DMPWgsPklpE_w6/edit)
