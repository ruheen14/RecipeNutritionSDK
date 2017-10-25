# RecipeNutritionSDK
# Overview
In this modern world,everyone has become very health conscious.Everyone is very particular to keeping their daily calorie intake and nutrition in check and to achieve that each of us is getting more and more inclined towards preparing our own homemade recipes according to what suits our needs the best.Since it is a very tedious task to manually count the calories and nutrition  of each and every ingredients in a recipe one prepares,this system will help to easily calculate the total calories and nutrition information of the food per serving.

# High Level Design
So this is how it will be achieved:
The user will enter the name of each ingredients used in their recipe and the USDA search API
<https://ndb.nal.usda.gov/ndb/doc/apilist/API-SEARCH.md> will return a list of types of ingredient and an unique identification number for each of items in the list(Ndbno).

The user then enters the unique identification number(Ndbno) to get the nutrition value and calories for the particular ingredient he is interested in which is returned by the USDA report API <https://ndb.nal.usda.gov/ndb/doc/apilist/API-FOOD-REPORT.md>

Following the above directions rest of ingredients in the recipe are searched by the user which in turn returns a value for each ingredients and the user clicks the Calculate button.

The Calculate button then calls a method which will return the total calories and nutritional value for the recipe.



# Dependencies
USDA Search API <https://ndb.nal.usda.gov/ndb/doc/apilist/API-SEARCH.md> and USDA Report API <https://ndb.nal.usda.gov/ndb/doc/apilist/API-FOOD-REPORT.md> which is explained above how it will work.

DynamoDB API <http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/QueryingJavaDocumentAPI.html>
Each row in the table will contain a recipe which will include the list of ingredients used in the recipe with their respective ndbno which will enable the user to enter and search for the latest nutrition value and the total calories per serving.
# Features
-Ingredients,Calories, Multiple Page Support, Sorting options, 
