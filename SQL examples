-- Select the top 10 causes of death and their corresponding counts
SELECT Cause_of_Death, COUNT(*) AS Death_Count
FROM Causes_of_Death
GROUP BY Cause_of_Death
ORDER BY Death_Count DESC
LIMIT 10;

-- Calculate the average age at the time of death for each cause
SELECT Cause_of_Death, AVG(Age_at_Death) AS Average_Age
FROM Causes_of_Death
GROUP BY Cause_of_Death;

-- Filter the dataset to include only deaths caused by specific causes
SELECT *
FROM Causes_of_Death
WHERE Cause_of_Death IN ('Heart Disease', 'Cancer');

-- Find the cause of death with the highest number of deaths in a specific year
SELECT Year_of_Death, Cause_of_Death, MAX(Death_Count) AS Max_Deaths
FROM (
    SELECT Year_of_Death, Cause_of_Death, COUNT(*) AS Death_Count
    FROM Causes_of_Death
    GROUP BY Year_of_Death, Cause_of_Death
) AS Subquery
GROUP BY Year_of_Death;
