# Amazon_Vine_Analysis
Analyze reviews written by paid members of the Amazon Vine program to determine whether or not there is bias.

## Overview:
The purpose of this project is to analyze reviews on Amazon products and determine if there is bias between reviews from Amazon Vine program members (who are paid for reviews) and non-members (who are not paid for reviews). The goal is to determine the percent of reviews that have 5-star ratings for both Vine members and non-members.


Amazon Reviews dataset: [Link](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Lawn_and_Garden_v1_00.tsv.gz)

## Methods:
1)	Created an AWS database instance to connect to Postgres.
<img src="https://github.com/eoweed/Amazon_Vine_Analysis/blob/main/Images/AWSdatabase.png"/>

2)	Created a database in the AWS server with four tables.
    a.	review_id_table
    b.	products_table
    c.	customers_table
    d.	vine_table

3)	Extracted the Amazon Reviews dataset.

4)	Transformed the dataset into dataframes that match the four tables in the database.
<img src="https://github.com/eoweed/Amazon_Vine_Analysis/blob/main/Images/CreateTables.png"/>

5)	Wrote the tables into the database.
<img src="https://github.com/eoweed/Amazon_Vine_Analysis/blob/main/Images/WriteTables_to_Database.png"/>

6)	Analyzed reviews from Vine members and non-Vine members.
<img src="https://github.com/eoweed/Amazon_Vine_Analysis/blob/main/Images/Vine_vs_NonVine_Results.png"/>


## Results:
* Vine Members:
   * Total Number of Reviews: 386
   * Total Number of 5 Star Reviews: 176
   * Percent of 5 Star Reviews: 46%
* Non-Members:
   * Total Number of Reviews: 48,717
   * Total Number of 5 Star Reviews: 24,026
   * Percent of 5 Star Reviews: 49%


## Summary:
Overall, it seems that there is no bias between reviews from Vine members and non-members. The percentage of 5-star reviews from both groups is between 45%-50% so it seems unlikely that Vine members give a higher number of 5 star reviews compared to non-members. However, it may be helpful to analyze the average rating given by each group in order to determine if there is a difference in average rating for each product.
