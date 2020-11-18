# TIKI SCRAPING PROJECT
![](https://a.ipricegroup.com/media/Tiki_1.jpg)

## Project overview
Tiki (short for “Tìm kiếm & Tiết kiệm”, which means “Search & Save”) is one of the Big Four e-commerce markets and the most trusted B2C platform in Vietnam.

Scraping tiki was the first project in Machine learning bootcamp at Coderschool as one of the most important tasks of a data scientist / data analyst is collecting the data.

## Database diagram
In this project, we tried to scrape the product information from Tiki accrossing all categories.
The database consists 2 tables: 
![](https://i.imgur.com/Lo1hJM3.png)

## How I collected information
**Step 1:** From Tiki homepage, we got 16 main categories.

**Step 2:** After getting 16 main categories, our code using recursion will go to each category, get its sub-categories in each tier until it reaches the last tier and automatically saved in sqlite database.
We got 3,195 categories in total which are saved in ```category``` table.

**Step 3:**
Get URLs of the last layer of sub-category by joining 2 tables and get only the unmatched rows.

**Step 4:**
Go to each URL in the last layer to get product information and automatically save in ```product``` table.

## Issues
When scraping product information, tiki shows only 21 pages for each category so I could not scrape all products in a category which has more than 1,092 products.


