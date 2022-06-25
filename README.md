# Amazon Vine Analysis

### Overview of the analysis: 

This analysis is done on Amazon Reviews (comprised of both paid reviews known as Vine and non paid reviews) to determine if there is any bias toward favorable reviews from Vine members in the given dataset.

What we will do is to compare the Vine Reviews data and non-Vine reviews data.

### Results:
I had a Tab Separated file of all the reviews for the category of 'Shoes' that we read into PySpark and created a dataframe from.
I, then created the Vine_table with only relevant columns as the structure shown below:

![Vine_table_columns](/images/M16_del2_1.png "Vine Table Column Headers")

From there, I filtered the data to only assess the reviews with over 20 votes, then I narrowed down to the reviews where the percentage of helpful_votes was equal or greater than 50%.

Then I split this dataframe between Vine reviews and non-Vine reviews to be able to compare the two.

The factors that the two subsets were compared are :
- the total number of reviews
- the number of 5-star reviews
- the percentage 5-star reviews

The results are as follows:

#### Vine Reviews:
- How many Vine reviews were there? **22**
- How many Vine reviews were 5 stars? **13**
- What percentage of Vine reviews were 5 stars? **59.03**

#### Non Vine Reviews:
- How many non-Vine reviews were there? **26987**
- How many non-Vine reviews were 5 stars? **14475**
- What percentage of non-Vine reviews were 5 stars? **53.64%**

![Vine_Reviews](/images/M16_del2_2.png "Vine Reviews")

![Non_Vine_Reviews](/images/M16_del2_3.png "Non-Vine Reviews")


### Summary:
From what I understand from the proportion of paid to unpaid reviews, since the number of paid reviews are much less that non-paid reviews, they would not change the overall outcome, but even if they did, by comparing the percentage of the 5star reviews by the paid reviewers to unpaid reviewers, we can see that being paid did not make them give a 5star review, and it seems that their reviews and ratings are honest. As we can see the percentage of 5star vine reviews are 59% where as the percentage of 5star non-vine reviews are 53% which is not far from the paid reviews.

We only compared the 5 star reviews, but as an additional analysis, we could also compare the numbers for 4star, 3star, 2star or 1star reviews for Vinr-reviews with non-Vine reviews.

-------------------

## Deliverable 1:
- Amazon Dataset was read and a dataframe was created from it.
- Then four dataframe were created with the fields based on the sql schema.
- PostgreSql database and the four tables where created using the schema.
- The four dataframes then were written into the SQL tables.
- Screenshots of the partial data within the tables can be found in the images folder in the github: click [here](/images/ 'images')
