# tiki-scrapping
Tiki scrapping is a project which I use Selenium Web Driver to extract all information of products from the Tiki website and synthesize as a .csv file (similar to the Excel file). This project is done in Google Colaboratory Notebook using Python language

![image](https://user-images.githubusercontent.com/97778235/158594933-1694234c-090a-4858-86c7-ab5778711a43.png)


## **Overview**

Tiki is considered as one of the top 4 ecommerce platforms with high number of customers in Vietnam, along with Shopee, Lazada and Sendo. Founded in 2010, Tiki has always strived to improve product quality as well as service with a view to optimizing customer experience while shopping with fast delivery in 2 hours.
Tiki has 3 subsidiaries including Tiki Corporation, Tiki Smart Logistics and Tiki Trading which all support Tiki operations to support customers from product segmentation to final delivery and post-purchase activities from customers

## **Problem Statement**

When I buy things at any ecommerce platform such as Tiki, I have to scroll page by page and click any product and check the name, price, image, thumbnail, ratings and so on. The fact that you have to scroll page by page is time-consuming. I can spend nearly 2 hours just only scrolling the pages. So I am thinking how about scrapping product information all at once and size them up as a Excel file (.csv) file to check the information easier. 

## **Methodology**
The methodology can be divided into 6 steps which are included in installing Selenium and other libraries such as Regex, Pandas; configuration to the driver and steps to open and close the driver; function to get info from one product, function to scrape all information product from  one page, function to scrape all information product from one main category, function to scrap all the products

### Installing Selenium and libraries including Regex, Panda and Time

#### Installing Selenium
![image](https://user-images.githubusercontent.com/97778235/158594777-bdf59b41-da5e-42c1-a3a3-73a4f9596cb3.png)

#### Installing Regex, Panda and Time
![image](https://user-images.githubusercontent.com/97778235/158596294-bb456ee4-1389-4206-ad6b-c3a43d26158b.png)

### Configurating the Driver and function to open and close the driver to start scrapping

#### Configurating the Driver

![image](https://user-images.githubusercontent.com/97778235/158596759-89f857dd-a1a7-4ea9-b30f-4f01cd7c1397.png)

#### Function to open and close the driver

![image](https://user-images.githubusercontent.com/97778235/158596869-5df4d123-85af-46bd-a7d2-071b1818e455.png)

### Function to get information from one product

For this function, I create a dictionary named info and include the keys such as product name, price, thumbnail, product_url, discount, freeship, badge "re hon hoan tien", freeship and installment icons

![image](https://user-images.githubusercontent.com/97778235/158597419-1575b3e5-e249-4444-8b9d-7c484d801c92.png)

For full function, you can check at the Final file as following link: https://github.com/hh7sag/tiki-scrapping/blob/main/%5BProject%5DTiki_WebScraper_Huong_Huynh_Final.ipynb

### Function to get information from all products for one page

For this function, I use for-loop to append more product info in the original function to scrap 1 product  
![image](https://user-images.githubusercontent.com/97778235/158597895-0fb70400-b379-4923-9fa5-f27c9378027c.png)

### Function to get information from all products for one main category 
![image](https://user-images.githubusercontent.com/97778235/158598276-1ebba36b-ea37-408b-8e8a-deac22e020c0.png)

For full function, you can check at the Final file as following link: https://github.com/hh7sag/tiki-scrapping/blob/main/%5BProject%5DTiki_WebScraper_Huong_Huynh_Final.ipynb

### Function to start scrapping all information

After writing all supporting functions, this function serves as a main function to scrap the information all at once
![image](https://user-images.githubusercontent.com/97778235/158598680-680e09d9-6687-44d9-8c11-1aca261d937c.png)

## **Result**
After scrapping the needed data, I create a dataframe which converts into a csv file and set the number of records up to 50 products

![image](https://user-images.githubusercontent.com/97778235/158599060-4cb6d5d2-577f-46da-9662-2e45301564c5.png)

So, there you have it, a full dataframe of all Tiki products in just a page, which helps me choose the product much faster.

For more information, you can check at my Google Colab link: https://colab.research.google.com/drive/18GSwNTrxfJrwMec73FSorJZY5yzJUbQ7?usp=sharing

