# SQL-Project 


SELECT  
AVG(Profit) AS Profit, 
AVG(Discount) AS Discount, 
AVG(Sales) AS Sales
FROM `optimum-entity-358419.Walmart_data.Walmart` 

![Image](https://user-images.githubusercontent.com/102627671/190207758-858c58de-6caf-4dcc-8474-f468ecc7dbe9.png)
--I got the average profit for sales, discount, and sales

SELECT 
  AVG(Profit) AS Average_Profit,
  State
FROM
  `optimum-entity-358419.Walmart_data.Walmart`
  GROUP BY State
ORDER BY State ASC

![Image](https://user-images.githubusercontent.com/102627671/190208019-ebb538f8-1d76-4cff-bd6d-3353ab2435a3.png)
--I then got the average profit per state
SELECT COUNT(*) AS customers, 
case
  when Customer_Age between 40 and 49 then 'fortys'
  when Customer_Age between 50 and 59 then 'fiftys'
  when Customer_Age between 60 and 69 then 'sixtys'
  when Customer_Age between 70 and 79 then 'seventys'
  when Customer_Age between 80 and 89 then 'eightys'
  when Customer_Age >=90 then 'ninetys'
  END AS age_range,
  AVG(Profit) AS Av_Profit
FROM
  `optimum-entity-358419.Walmart_data.Walmart`
WHERE Customer_Age is NOT NULL
 GROUP BY age_range
![Screenshot 2022-09-14 11 18 36 AM](https://user-images.githubusercontent.com/102627671/190227887-54b878b0-59ee-4304-a549-34c11d2dad2c.png)
--I also got the average profit for ages 40-90
--I then uploaded my results to tableau public and made a visual with some extra data. https://public.tableau.com/app/profile/sierra.delgado/viz/WalmartRetailDataAnalysis_16627643836960/WalmartRetailDataAnalysis



