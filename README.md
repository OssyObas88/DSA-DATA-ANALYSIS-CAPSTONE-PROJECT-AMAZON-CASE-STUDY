# DSA DATA ANALYSIS CAPSTONE PROJECT
# AMAZON CASE STUDY
This is my project work after the training organised by DSA to test our journey thus far in order to be able to score us for the next level in our journey in Data Analysis. This project is part of the DSA Data Analysis Capstone and focuses on performing Exploratory Data Analysis (EDA) on Amazon product review data. The objective is to extract insights that can inform product development, pricing strategy, and customer engagement using Microsoft Excel.
This repository contains the complete analysis, insights, and dashboard for **Case Study 1: Amazon Product Review Analysis** from the DSA Data Analysis Capstone Project file.

## Project

As a Junior Data Analyst at RetailTech Insights, I was tasked with analyzing Amazon product review data to uncover insights that can help with product improvement and customer engagement strategies.

## Dataset Description

The dataset includes:
- Product details (name, category, price, discount, rating)
- Customer engagement (review count, review content, etc.)
- 1,465 product entries with 16 columns

## Tools Used

- Microsoft Excel (Pivot Tables, Charts)
- Calculated Fields
- Excel Dashboard

## Steps Applied and some Excel Functions Used

- I collected my data from the LMS and uploaded to my excel worksheet after which I first cleaned the data by removing duplicates on product ID using remove duplicates under the data tool group.
- I counted the blanks on the dataset by using the **count blank** function to know the number of blank cells in the dataset. 
- To split the category into separate columns dues to the lenght of the data, I used **text to columns** function and then delimeter to split the column into 4 separate columns aside the major category.
- To generate **Price Range Bucket**, the excel function used was =IF(I2<200,"<₹200",IF(OR(I2=200,I2<=500),"₹200 - ₹500",">₹500"))
- To generate **Average Discount**, the excel function used was =([@[Actual_price]]-[@[Discounted_price]])*100
- To generate **Discount Range**, the excel function used was =IF([@[Discount_percentage]]>=50%,"50% or more","<50%")
- To generate **Rating and Review**, the excel function used was =AVERAGE([@Rating]+[@[rating_count]]/1000)
- To generate **Discount Bucket**, the excel function used was =IF([@[Discount_percentage]]<=10%,"0-10%",IF([@[Discount_percentage]]<=20%,"11-20%",IF([@[Discount_percentage]]<=30%,"21-30%",IF([@[Discount_percentage]]<=40%,"31-40%",IF([@[Discount_percentage]]<=50%,"41-50%",IF([@[Discount_percentage]]<=60%,"51-60%",IF([@[Discount_percentage]]<=70%,"61-70%",IF([@[Discount_percentage]]<=80%,"71-80%",IF([@[Discount_percentage]]<=90%,"81-90%","91-100%")))))))))
- To generate **Total Potential Revenue**, the excel function used was =actual prize*Rating count.

## Analysis Tasks Completed

- Average discount percentage by product category
- Product count per category
- Total reviews per category
- Highest rated products
- Comparison of actual vs discounted prices by category
- Products with highest number of reviews
- Distribution of product ratings
- Revenue analysis (actual price × rating count)
- Discount and rating correlation
- Top products by combined score (rating & reviews)
- Products with discounts ≥ 50%
- Products with <1,000 reviews
- Price range buckets and category-based performance

## Key Insights

### Discount Analysis
- **Computers & Accessories** has the highest average discount at **53.2%**, followed by **Electronics** at **49.9%**.
- Some individual products have discounts as high as **94%**.

### Product Distribution
- **Home & Kitchen** category holds the most products (**448 items**).

### Review Count
- **Electronics** received the most total reviews (**14.2 million+**), indicating high customer engagement.
- **310 products** have fewer than 1,000 reviews, indicating low popularity or new listings.

### Rating Insights
- **Car & Motorbike** products have the highest average rating at **4.49**.
- The top products balance both high ratings and high review counts.

### Discount vs. Rating
- Products with higher discounts don't necessarily have the highest ratings — indicating price isn't the only factor affecting quality perception.

### Conclusion
- **Focus areas for marketing**: Promote top-rated but low-reviewed products to increase visibility.
- **Inventory strategy**: Analyze underperforming Electronics to reduce low-rated, high-discount items.
