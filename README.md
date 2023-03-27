# coromandel-web-scrapping

This code does the web scraping using Python with the help of Selenium and BeautifulSoup libraries. The purpose of this code is to scrape product details from the website https://www.coromandel.biz/product-services/plant-growth-regulators/.

The first section of the code imports the required libraries such as Selenium, BeautifulSoup, Pandas, and time. It then opens a Chrome browser using the Selenium webdriver and navigates to the specified URL.

Once the page is loaded, the code scrolls down to the bottom of the page using the execute_script method of Selenium. The page source of the loaded web page is then passed to BeautifulSoup for parsing.

The BeautifulSoup object is then used to find all the product links on the page by searching for div elements with the class name "image-video-section overflow-hidden". The URL of each product is stored in the "productlinks" list.

The next section of the code loops through each product URL in the "productlinks" list and extracts the required product details from each page. The product details extracted include the product name, brand name, pack size, detail, dose, features, image link, and product link.

The extracted product details are then stored in a dictionary with the corresponding keys and values. This dictionary is appended to the "data" list.

After extracting all the required details for all the products, the "data" list is converted to a Pandas DataFrame using the from_dict method of Pandas.

Finally, the new DataFrame is displayed with the help of the head() method of Pandas, which displays the first 50 rows of the DataFrame.
