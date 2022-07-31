
# Database Task

 1-Which drink has the highest calories from the dataset ?

SELECT Beverage_category, Beverage, MAX(Calories) FROM drinkmenu;

![App Screenshot](https://raw.githubusercontent.com/muhammad7saeed/Database-Task--eT3-/c8f3d5e4f56317a4f714fafa8983a37dfb2691aa/DataBase%20Task/1Query.png)

----------------------------------------------------------------------------------------------

2. What is the average calorie amount for each drink category ?

SELECT Beverage_category, AVG(Calories) FROM drinkmenu GROUP by Beverage_category

![App Screenshot](https://raw.githubusercontent.com/muhammad7saeed/Database-Task--eT3-/c8f3d5e4f56317a4f714fafa8983a37dfb2691aa/DataBase%20Task/1Query.png)

-----------------------------------------------------------------------------------------------

3-Which drinks have below average calorie amount ?

SELECT drinkmenu.`Beverage_category`,`Beverage`,`Calories` FROM drinkmenu 

join (SELECT  Beverage_category ,AVG(Calories) as AVarege FROM drinkmenu GROUP by Beverage_category) as test
on test.Beverage_category = drinkmenu.`Beverage_category`

WHERE drinkmenu.Calories < test.AVarege;

![App Screenshot](https://raw.githubusercontent.com/muhammad7saeed/Database-Task--eT3-/c8f3d5e4f56317a4f714fafa8983a37dfb2691aa/DataBase%20Task/3Query.png)

--------------------------------------------------------------------------------------------------
