# Multi-Class Text Classification using PySpark

For this project, *Amazon Reviews Dataset* is used. In the file reviews_devset.json, each line corresponds to a review in JSON format. The following entries are contained in each dictionary:

```
Sample review:
{
    "reviewerID": "A2VNYWOPJ13AFP", 
    "asin": "0981850006", 
    "reviewerName": "Amazon Customer \"carringt0n\"", 
    "helpful": [6, 7], 
    "reviewText": "This was a gift for my other husband.  He's making us things from it all the time and we love the food.  Directions are simple, easy to read and interpret, and fun to make.  We all love different kinds of cuisine and Raichlen provides recipes from everywhere along the barbecue trail as he calls it. Get it and just open a page.  Have at it.  You'll love the food and it has provided us with an insight into the culture that produced it. It's all about broadening horizons.  Yum!!", 
    "overall": 5.0, 
    "summary": "Delish", 
    "unixReviewTime": 1259798400, 
    "reviewTime": "12 3, 2009", 
    "category": "Patio_Lawn_and_Garde"
}
```

where:

- **reviewerID** - string - the ID of the author of the review
- **asin** - string - unique product identifier
- **reviewerName** - string - name of the reviewer
- **helpful** - array of two integers [a,b] - helpfulness rating of the review: a out of b customers found the review helpful
- **reviewText** - string - the content of the review; this is the text to be processed
- **overall** - float - rating given to product asin by reviewer reviewerID
- **summary** - string - the title of the review
- **unixReviewTime** - integer - timestamp of when review was created in UNIX format
- **reviewTime** - string - date when review was created in human readable format
- **category** - string - the category that the product belongs to

## Task

This project is divided into three parts:

1. Part 1) RDDs
    -   Calculating chi-square values using RDDs and transformations. Writing the output to a file *output_rdd.txt*.
2. Part 2) Datasets/DataFrames: Spark ML and Pipelines
    -   Building a **Spark ML Pipeline** to convert the review texts to a classic vector space representation with TFIDF-weighted features based on the Spark DataFrame/Dataset API
3. Part 3) Text Classification
    -   Extend the pipeline from Part 2 to learn a model that can predict the product category from a review's text.


*NOTE that this project was a requirement of **Data-intensive Computing** course in **Data Science program** at **Technical University of Vienna**.*
*The tasks were implemented using **PySpark** and **jupyter notebook 6.0.3** in **18 node Hadoop Cluster at TU Wien***
