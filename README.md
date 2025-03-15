# The Rise and Fall of Keto in the Early 21st Century 
By: Allyson Ting (a2ting@ucsd.edu)

---
## Introduction 

The 21st Century has seen many fad diets pass in and out of the spotlight. In the 2010s, the Keto Diet and its idea of high-fat, moderate-protein, and low-carbs took that spotlight, even becoming the most Googled diet in the United States in 2020. Specifically, over 50% of calories should be from fat, over 10% from protein, and the remaining from carbohydrates. As this new definition of "health" invaded the media, the food people cooked may have changed to fit this standard, even if they were not specifically trying to eat keto. 

**How did the keto diet influence home-cooking?**
Besides percentages of fat and carbs, what characteristics best indicate whether a recipe is ketogenic or not?

Answering these questions is not only useful for bloggers looking to label their recipes as keto to gain traction, nor just for people trying to easily identify keto recipes to follow the diet, but investigating the relationship between the keto diet and home-cooking also offers insight into the influence of media on people's relationship with food. A more abstract question for this project: How does media end up in our mouths?

In this project, we analyze two datasets, `recipes` and `interactions`, from [food.com](https://www.food.com/). Our datasets contain information about recipes and recipe reviews spanning from 2008 until 2018 (more details below). This data was originally collected to experiment with a model that generates personalized recipes as explained in Majumder et al's research paper, [Generating Personalized Recipes from Historical User Preferences](https://cseweb.ucsd.edu/~jmcauley/pdfs/emnlp19c.pdf).

`recipes`, has 83782 rows, one for each recipe. 
| Column | Description |
| ----------- | ----------- |
| 'name' | recipe name |
| 'id' | recipe ID |
| 'minutes' | minutes to prepare recipe |
| 'contributor_id' | user id who submitted this recipe |
| 'submitted' | date recipe was submitted |
| 'tags' | Food.com tags for recipe |
| 'nutrition' | nutrition information ℹ️|
| 'n_steps' | number of steps in recipe |
| 'steps' | text for recipe steps, in order |
| 'description' | user-provided description |
| 'ingredients' | list of ingredient names |
| 'n_ingredients' | number of ingredients |

ℹ️ (calories (#), total fat (PDV), sugar (PDV) , sodium (PDV) , protein (PDV) , saturated fat (PDV) , and carbohydrates (PDV))

 `interactions` has 731927 rows, each corresponding to a rating left for a recipe. 
 | Column | Description |
| ----------- | ----------- |
| 'user_id' | user ID |
| 'recipe_id' | recipe ID |
| 'date' | date of interaction |
| 'rating' | rating given |
| 'review' | review text |

The most relevant columns for our investigation are `'submitted'`, `'date'`, `'nutrition'`, `'tags'`, `'n_steps'`, and `'n_ingredients'`, all described above. 
