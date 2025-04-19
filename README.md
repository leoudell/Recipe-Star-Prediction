**Authors:** Sophia Papadopoulos and Leo Udell

**Emails:** ___ leoudell@umich.edu

# Introduction 
Picture this. You come home from a long day at work at the world's best data science company. All you want is a quick bite, but what are the odds this meal will be 5 stars? What is the relation between complexity and star ratings? This analysis explores a dataset of over 730,000 reviews on food.com to determine the relationship between highly rated recipes and recipe complexity. We have defined how complex a recipe can be based on how long it takes to prep and cook, the number of different ingredients, and the number of steps. By analyzing this complexity, we can help chefs optimize the complexity of their recipes for better ratings and different audiences.

**Total Rows in Dataset:** _
| Column Recipe in Dataset    | Description |
|-------------|-------|
| 'name'   | Recipe name|
| 'minutes' | Minutes to prepare recipe |
| 'n_steps' | Number of steps in recipe    |

| Column Rating in Dataset    | Description |
|-------------|-------|
| 'user_id'   | User ID |
| 'rating' | Star rating given by user |

# Data Cleaning and Exploratory Data Analysis
## Data Cleaning
1. Merging the Datasets
2. 
## Univariate Analysis
This plot shows the distribution of ratings between recipes. As shown by the plot, most of the recipes have a 5-star rating. There are also a few recipes with a 0 rating, indicating that the user did not leave a rating for their posted comment. This does not mean that the user rated the recipe poorly, but that they chose not to rate the recipe. Given our goal, keeping these 0-star ratings would give inaccurate final results, so we chose to drop these recipes from our dataset. 
## Bivariate Analysis
This plot measures the average rating, number of steps, and minutes to prepare each recipe in the dataset.
## Interesting Aggregates
When constructing the bivariate analysis of the dataset, we were curious about the recipes with the longest preparation time. We came across one recipe with a strange title. Taking over 1 million minutes, "How to Preserve a Husband" has 2 ingredients (cream and peaches) and 2 five-star reviews. 
## Imputation
While cleaning the data, we found that there are no missing values in the dataset. For some recipes, there are 0 ratings for that recipe and that would then be converted to a NAN value. Due to the model we created, the recipes with zero reviews are not useful and were removed. 
# Problem Identification
What is the average rating for a recipe based on its "complexity"? We have defined recipe "complexity" as the number of ingredients, the number of minutes it takes to complete, and the number of steps included. In order to do this, we constructed a regression model to predict the recipe's start rating of 0 - 5. 

# Baseline Model

# Final Model
