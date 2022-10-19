# Amazon_Vine_Analysis

## Overview of the Analysis
For this analysis, I focused on analyzing paid reviews through Amazon Vine versus unpaid reviews for a product set of physical video games. Using PySpark, I performed the ETL process to extract, transform, and load the data into pgAdmin using an AWS RDS instance. I used PySpark to continue my analysis on whether there is a bias toward favorable reviews in my video game dataset. 

## Results 

There were a total of 40,565 reviews for the video game dataset. 
- 94 reviews were paid
- 40,471 reviews were not paid
- 51% of paid reviews, or 48 reviews, were 5 stars
- 38% of unpaid reviews, or 15,663 reviews, were 5 stars 

In order to run the analysis, I filtered the data for more than 20 total votes where more than 50% of those votes were "helpful." I then created two separate dataframes, one for paid reviews and one for unpaid reviews. Using the seperated dataframes, I ran the analysis for 5-star reviews in both categories. 

![paid reviews](https://github.com/noorsami12/Amazon_Vine_Analysis/blob/0d4ca92ee0d06e80074a9a0b54c242367ea37c35/paid%20vine%20reviews.png)
![unpaid reviews](https://github.com/noorsami12/Amazon_Vine_Analysis/blob/0d4ca92ee0d06e80074a9a0b54c242367ea37c35/unpaid%20amazon%20reviews.png)


## Summary

Based on the analysis of the video game dataset, there could potentially be a positivity bias in paid reviews. Paid reviews are significantly higher at 51% with 5 stars, while 38% of unpaid reviews are 5 stars. That being said, the analysis is not in depth enough to fully conclude a positivity bias. In order to deepen the analysis, we could run a similar analysis to find the percentage of 1-star ratings. It’s possible that there are simply less 5 star ratings by unpaid reviewers because the amount of unpaid reviews are so much larger at over 40,000 reviews, while paid reviews are just under 100. Comparing the number of 1-star reviews would shed more light on the potential of a positivity bias. If paid reviewers are more likely to rate a product 5 stars, it follows that they would also be less likely to give the product the very low rating of 1 star.

Additionally, further analysis should be done on other product datasets to see if there is a positivity bias trend across products. 
