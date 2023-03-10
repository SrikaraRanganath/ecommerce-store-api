# ecommerce-store-api
## Routes
###### /api/v1/products/static 
This is a static route which returns all the products on the mongoDb database
###### /api/v1/products/
This is the main route to which we can speficy the query parameters for sorting ,selection, numeric filtering and paging.

*Note: Store data can be found in products.json*

## Query Options

| Function | Parameter | Description | Example |
| --- | --- | --- | --- |
| Filtering | /attribute=value | Returns all featured products | /company=ikea : returns all products from ikea |
| Sorting | /sort=value1,-value2 | Returns sorted list of products according to the parameter options. - is used to indicate descending | /sort=name,-price : returns all products sorted in ascendign order of name and decreasing price values |
| Selecting | /fields=value1,value2 | Returns all products with only the selected fields | /fields=company,name : returns all products with only name and company |
| Numeric Filtering | /numericFilters=field op value | Returns all products with the filter applies | /numericFilters=price>30 : returns all products with their price above 30|
| Paging | /page=value&limit=value | Returns all products in pages with limit specifying no of products in a page| /page=4&limit=10 : returns the 4th page with 10 products |

## Usage
1. Install the packages using 
```
    npm install
```
2. Create a .env file and enter the following 
```
    MONGO_URI = <your_mongo_uri>
    PORT = <your_port>
```
3. Start the server using 
```
    npm start
``` 
