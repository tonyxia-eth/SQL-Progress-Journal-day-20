# SQL-Progress-Journal-day-20

# Day 20 – Subquery Breakthrough 🎯

## ✅ What I Practiced
- Scalar subqueries using `MAX()` and `AVG()`
- Comparing values in `WHERE` and `HAVING` clauses
- Writing clean, readable SQL without shorthand
- Logical breakdown of inner (subquery) and outer queries
- Real-world filtering with nested data references

## 🧠 Key SQL Concept
Subqueries can return a single value and be used in conditions like:

```sql
SELECT players.first_name, players.last_name, salaries.salary
FROM players
JOIN salaries ON players.id = salaries.player_id
WHERE salaries.year = 2001
  AND salaries.salary < (
      SELECT MAX(salary)
      FROM salaries
      WHERE salaries.year = 2001
  )
ORDER BY salaries.salary DESC
LIMIT 10;


💡 What I Learned
Subqueries don’t have to be scary when broken down logically.

I now understand the difference between inner and outer queries.

This lesson built directly on top of JOIN + GROUP BY logic from earlier days.

🔥 What’s Next
Master subqueries inside HAVING clauses

Take on Task 8 from the CS50 Moneyball project

Begin connecting subquery logic to real data engineering tasks

#100DaysOfSQL #DataEngineering #SQLLearning #CS50 #MenInTech #Subqueries #SQLPractice
