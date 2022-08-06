# Module 16 Challenge

## Amazon Web Services 

### Overview

*Background*

BigMarket is a startup that helps companies optimize their marketing efforts. An account manager at BigMarket, Jennifer, is working on a project for a client, Sellby. Sellby is a retail website and is working on a hefty project: releasing a new catalog of products. Before they release these new products, they would like to have reviews of their products compared with product reviews from their competitors. Sellby would also like to know if it is worth the cost to gift free products to select reviewers. Since the data has exceeded the capacity of operational databases, it is now considered "big data"; therefore, the data will need to be translated and edited to make the data into a meaningful guide to the client, Sellby. 

*Purpose*

Since the work with Jennifer on the SellBy project was successful, another, larger project has been assigned. Now we will be analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

This project will utilize approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. One of the datasets will be chosen, and PySpark will be used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, PySpark, Pandas, or SQL will be used to determin potential bias toward favorable reviews from Vine members in the dataset. Then, a summary will contain the analysis for Jennifer to submit to the SellBy stakeholders.

## Software

- Google Colab
- Spark—PySpark 
- Amazon Web Services (AWS)
  - Relational Database Service (RDS)—PostgreSQL 
  - Simple Storage Service (S3)
- pgAdmin 4


[Successful Linkage between AWS and PgAdmin](https://user-images.githubusercontent.com/102566199/183231546-16185402-428b-4070-84e3-566e65f537f9.png)

## Results

![Results](https://user-images.githubusercontent.com/102566199/183230977-cda965cb-e65a-440c-b83c-c7e6a49f1cca.png)


There was a total of 9,002,021 reviews. 

[Code: Total Number of Reviews](https://user-images.githubusercontent.com/102566199/183230820-6293efe1-e1c0-4a9c-914f-f6d326f2cef3.png)

- How many Vine reviews and non-Vine reviews were there?

| Vine Reviews | Non-Vine Reviews |
| ------------ | -----------------|
| 17,481       | 8,984,400        |

-------------------------------------------------------

There was a total of 4,824,725 5-star reviews.

[Code: Total Number of 5-Star Reviews](https://user-images.githubusercontent.com/102566199/183230842-b1e69082-2039-4d83-9a11-6003a9e0b65b.png)

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

| Vine Reviews | Non-Vine Reviews |
| ------------ | -----------------|
| 6,522        | 4,818,203        |


[Code: Percent of 5-Star Vine Reviews](https://user-images.githubusercontent.com/102566199/183230883-47e7c8e6-0743-4c2f-ab21-2699dee01568.png)

[Code: Percent of 5-Star Non-Vine Reviews](https://user-images.githubusercontent.com/102566199/183230944-3506af02-2c36-4d7c-81d0-c3c6834e65b0.png)


- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

| Vine Reviews | Non-Vine Reviews |
| ------------ | -----------------|
|  37.3%       |    53.6%         |

----------------------------------------------------


## Summary

*Bias: Not Present*

Based on the results above, there was no bias present within the Vine program. The non-Vine Reviews (unpaid reviews) are in higher quality and there are more with a 5-star rating. The results do not show that Vine is doing significantly better than non-Vine, so I would not conclude on any bias being apparent, at this level of analysis. 

*Additional Analysis to Support Findings*

In the future, more analyses should be run to possibly filter other columns of the dataset that might lead to a better understanding of the data. The verified purchase column would be helpful to perform this on because by comparing the ratings on verified purchases for both paid and unpaid reviews. It would also be helpful to more carefully track which users are leaving the most reviews. This could help to verify that the reviews are "real" and that the reviewer actually bought the product. 

A useful filter would also be to search through the reviews and determine how rating differ from each other. If the paid reviews (Vine reviews) were higher on similar products, then there might be a possiblity of bias present. 
