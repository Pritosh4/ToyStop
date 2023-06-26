# ToyStop
ToyStop is an interactive dashboard that can visualize the data corresponding to the trends of the sales of toys on the Amazon India website and suggest appropriate toys based on user-chosen filters and requirements.

## Project Link and How to Use?
[Dashboard Link](https://public.tableau.com/app/profile/pritosh8817/viz/Book1_16782670778430/Dashboard1)

Once you click the link and open the dashboard you will notice 2 tables. The table at the bottom shows the Top 10 Most Bought Toys on the website, if you wish to directly go for the bestseller, then you can click the table cell of the toy you want, and clicking the cell will render the product page on the top right webpage element so that you can take a look at the product and see what it is (*This will not work on the online dashboard available on Tableau public as it will show an error as "www<span></span>.<span></span>amazon.<span></span>in refused to connect". This is a result of the Amazon India website's security policy, which intentionally uses the X-Frame-Options header to prevent cross-origin framing (embedded in <iframe>). However, if you download the dashboard and open it on Tableau Desktop then you will be able to view the web page object*). After looking at the product if you wish to buy it then click the link that is also there in the tooltip and that will take you to the product page on Amazon India from where you can directly buy your toy.
The table on the top is the dynamic table that will change according to the requirements and filters that you want to put. On the right you will see all the filters that you can use to ensure you find the perfect toy.
- The `Country` filter allows you to choose toys that are manufactured in the country or countries that you choose. 
- The `Age` filter lets you choose the age of your child so that it only shows toys that have a recommended age below the age of your child.
- The `Rating` filter lets you set the minimum rating that you want for the toy. If you want a toy that has a rating of more than 4 stars then you set this filter to 4.
-  The `Reviews` filter allows you to choose the minimum number of reviews that the toy needs to have. Since it can be assumed that only people who have bought the item will have reviewed it so in a way this filter also allows you to choose the toys that have been bought by at least a certain number of people.
- The `Price` filter is the classic filter that lets you set your budget for the toy that you want to buy.

The 2 Legends that are below the filters show a visualization in the last column of the table.
- The `Price` legend gives you a visual representation of the price of the toy.
- The `Reviews` legend shows the number of reviews that the toy has received (or the number of people who have bought that particular toy).

## Screenshots

### Web Scraping
![image](https://user-images.githubusercontent.com/93176385/224318199-564e66f2-09fa-492e-a845-50f6c68f5e78.png)


### Analysis
![image](https://user-images.githubusercontent.com/93176385/224318112-766114ae-ef87-4605-93c4-d2469f0c4f62.png)

### Dashboard
![image](https://user-images.githubusercontent.com/93176385/224316817-acadda28-a8ff-440f-9f88-0fb77499c26c.png)



## Inspiration
After becoming an uncle recently, a challenge that I faced while trying to gift my nephew a toy was that I was not able to find the perfect toy for him. Being a perfectionist at heart, I wanted to find the perfect toy for him, but I found that the filtering options on the Amazon India website were not adequate in ensuring that I could find him the perfect one. I could not sort the ratings with a predefined condition that there were at least 500 reviews posted because the only option that they had was to sort in descending order of ratings and that meant that the first toy in the sorted order was one that had a single 5-star rating and since only 1 customer bought it, hence it obviously was not the perfect one. That is where I had the idea of ToyStop.

## Reflection
This was a 2-week long project wherein initially, I web scraped the necessary product information of all the toys available from multiple pages of the Amazon India website using `BeautifulSoup`. 

After getting the data and converting it into a `.csv` file, I loaded it into a `PostgreSQL` database and ran `SQL` queries on the data to answer questions like “Which toy was the bestseller?”, “Which toy was the highest rated having at least 500 reviews?”, “How many toys are available on the website on the basis of the minimum age required?”, etc. 

After this brief analysis, the data was loaded onto Tableau and the dashboard created allowed the user to choose the filters and criteria that they wanted to set allowing them a personalised suggestion on the toys that they can buy.
