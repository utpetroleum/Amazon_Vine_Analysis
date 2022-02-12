# Amazon_Vine_Analysis

## Overview of Project

### Purpose

In this project, we analyzed Amazon reviews written by members of the paid Amazon Vine program, specifically Video Games reviews. We use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then we used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. 

## Results

-	How many Vine reviews and non-Vine reviews were there?

Vine Total Reviews:

![Vine_total_reviews](https://user-images.githubusercontent.com/92401000/153729448-e5f09c24-ca0d-408d-ad8c-cd797fc06d76.PNG)

Non-Vine Total Reviews:

![nonVine_total_reviews](https://user-images.githubusercontent.com/92401000/153729450-342f7957-5a13-435a-8ba0-9deb83979e06.PNG)

There were a total of 94 Vine reviews and 40,471 non-Vine reviews.

-	How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

Vine 5 Star Reviews:

![Vine_5_star_reviews](https://user-images.githubusercontent.com/92401000/153729454-be4d5873-43c5-467c-9987-6e6c816141b0.PNG)

Non-Vine 5 Star Reviews:

![nonVine_5_star_reviews](https://user-images.githubusercontent.com/92401000/153729460-68c31c25-e898-4845-833e-022c20ed0cae.PNG)

There were a total of 48 Vines reviews that were 5 stars and 15,663 non-Vine reviews that were 5 stars.

-	What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

Vine 5 Star Percent:

![Vine_5_star_percent](https://user-images.githubusercontent.com/92401000/153729461-f1b0c4f9-1716-4d55-b40b-078d2a1e3da7.PNG)

Non-Vine 5 Star Percent:

![nonVine_5_star_percent](https://user-images.githubusercontent.com/92401000/153729469-c24d1a5f-013c-413d-9fa3-df4c25958f0d.PNG)

51.06% of Vine reviews were 5 stars and 38.70% of non-Vine reviews were 5 stars.

## Summary

Based on the results, there is positivity bias for reviews in the Vine program. Reviews in the paid Vine program were more likely to give 5 star ratings (51.06%) while reviews in non-Vine program were less likely to give 5 star rating (38.70%).

Another analysis we can perform to prove this bias is to filter both Vine and non-Vine dataframe to 1 star rating. If Vine 1 star rating percentage is less than non-Vine 1 star rating, we can infer there is bias in the reviews.
