# Notebook #2: K Nearest Neighbors and Normalization

## The Data
For this notebook, you will load a new data set dealing with cars :articulated_lorry: :blue_car: :red_car: :taxi: :bus: and fuel efficiency :fuelpump: (vehicles.csv - included in the repository) using Pandas and perform some subsetting operations.

The data is originally from here: https://www.fueleconomy.gov/feg/download.shtml

You can find a description of what each column is here: https://www.fueleconomy.gov/feg/ws/index.shtml#vehicle

This data has a lot of columns, and Pandas will abbreviate the output by default. To show all of the columns, you can change this property using the set_option() function as follows:

`pd.set_option('display.max_columns', 100)` <br>

## What you need to do: :exclamation:
You're going to write a function that can make k-Nearest-Neighbor predictions for the combined fuel efficiency ("comb08" column) based on **three predictor columns: the year, the number of engine cylinders, and the engine displacement in liters ("year", "cylinders", and "displ" columns)**.

Notebook #2 consists of the following exercises :muscle:. 

<b> Make sure you do the following </b>: [ 1 point each ]
1. **Work with the right subset** (both rows and columns, re-read the first paragraph under 'what you need to do'): 
  - You're not going to work with the whole data set, just the cars with <b>"Regular" listed in the "fuelType" column</b>, and only use the `year`, `cylinders`, `displ`, and our target `comb08` columns. So, to start, make this subset of the original data.
2. Check for null values in the target and predictor columns. 
    - If you have a null target value, you will need to throw that example out. 
    - If you have a null predictor value, you can either fill them in with something (like the mean/median) or you can drop those rows from the data set.
    - Useful functions here are `isna()`, `any()`, `fillna()`, `value_counts()` and `dropna()`. 
    - Describe in a markup cell what you decided to do with the null data and why.
3. Write up a k-nearest-neighbors function like the one you made for the iris data set in class. 
    - It should be able to make mpg ("comb08") predictions for new cars based on the year, cylinders, and displacement. 
    - You should also be able to specify what you want to use as k.
4. Demonstrate that your function works by making up some new values for hypothetical cars and using your function to display the predicted mpg ("comb08") for that car.
5. Make a copy of the data and normalize the training data using Z-score-- `copy()` will be useful here. 
    - Predict the mpg of a particular car using your k-nearest-neighbors function with both the normalized and non-normalized training data. 
    - Compare your results. 
    - Use a markup cell to describe and explain the differences in a few sentences.

To submit your work, copy the link to your github repository, it should look something like https://github.com/j23-cs167/notebook-2-yourgithubusername, and submit the link to the Blackboard assignment (please help me save a few clicks and make sure your link it clickable). 


## :white_check_mark: Grading: 
I will update the following rubric with your grade after you have completed the assignment.
### Rubric:
| Exercise #  | Points Awarded (out of 1)  | Notes |
| --------- | -------------------: | --------- |
| 1: subset      |        |    |
| 2: null        |        |    | 
| 3: knn         |        |    |
| 4: demo        |        |    | 
| 5: normalize   |        |    |
| <b>Total       |      /5  | </b>   |
