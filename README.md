# Amazon_Vine_Analysis
### Module 16 of Data Analytics Bootcamp

## Overview 

The purpose of this project is analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.

In this project, I looked at the reviews for Music products and used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset.


## Results

### How many Vine reviews and non-Vine reviews were there?
There were far more non_Vine reviews than Vine reviews. Specifically, there were only 7 Vine reviews that met our requirements of having over 20 total reviews, and having at least half of those total reviews be listed as helpful reviews. This is compared to the 105,979 non-Vine reviews that met this requirement. 

[]

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- Of the 7 Vine reviews we had, none of them were 5 stars. 
- Of the 105,979 non-Vine reviews, 67,580 of them were 5 star reviews. 

[]
### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
- Zero out of the seven Vine reviews had 5 stars, which is a whopping 0.0%.
- 67,580 out of the 105,979 non-Vine reviews had 5 stars, which is about 63.8%

## Summary

There is no way to accurately tell if there is positivity bias for reviews in the Vine program. With only seven total products with enough Vine reviews to meet our requirements, we can't predict any sort of bias with a set of data so small. However, it is worth noting that none of those seven products had a star rating of 5 stars, so early indications would suggest that there is no positivity bias, especially considering 63.8% of qualifying non-Vine products had a star rating of 5. 

It might be worth loosening the qualifications we set for product reviews. This is really the only way to get more Vine review data without ditching this dataset for another. Ultimately, I think the qualifications we set are important, as we want to make sure the reviews we are considering are, in general, legitimate. Therefore, I think the best course of action would be to look at a different dataset with the same qualifications that will provide far more than seven total Vine reviews. 
