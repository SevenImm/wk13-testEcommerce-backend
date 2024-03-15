# wk13-testEcommerce-backend
## Description
Internet retail, also known as e-commerce, plays a significant role within the electronics industry, as it empowers businesses and consumers alike to conveniently engage in online buying and selling of electronic products. In the latest available data from 2021, the industry in the United States alone was estimated to have generated the substantial amount of US$2.54 trillion, according to the United Nations Conference on Trade and Development. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. Due to the prevalence of these platforms, developers should understand the fundamental architecture of e-commerce sites.

## Installation
To install this application, clone the repository to your local machine:

```
To use this application, you need to have MySQL installed on your machine. Create and seed the database using the following commands:
## Create the database
```bash mysql -u root -p
source db/schema.sql
exit
```

### Categories
 - (GET) localhost:3001/api/categories
 - (GET) localhost:3001/api/categories/1
 - [POST] http://localhost:3001/api/categories
    - json: {"category_name": "My favorite Category"}
- (PUT) http://localhost:3001/api/categories/2
    - json: {"category_name": "Updated Category"}
- (DELETE) http://localhost:3001/api/categories/1

## Seed the database
```bash
npm run seed
Start the server using: npm start
```

## Database Models
The database contains the following models:

* Category: Categories for products, with fields for id (primary key, auto-incremented) and category_name.
* Product: Products being sold, including fields for id, product_name, price, stock, and category_id.
* Tag: Product tags for additional categorization, including fields for id and tag_name.
* ProductTag: A junction model for many-to-many relationships between Product and Tag.

## API Routes
The application supports the following API routes:

GET, POST, PUT, DELETE routes for categories, products, and tags.
Routes to view all categories/products/tags or a single category/product/tag.

Urls used in video:
### Products
- (GET)localhost:3001/api/products
- (GET) localhost:3001/api/products/1
- (POST) http://localhost:3001/api/products
    - json data: {"product_name": "My favorite Product", "price": 19.99, "stock": 15, "category_id": 1}
- (PUT)http://localhost:3001/api/products/1
    - json data: {"product_name": "Updated Product", "price": 29.99, "stock": 20, "category_id": 2}
(DELETE)http://localhost:3001/api/products/1



### Tags
- (GET) localhost:3001/api/tags
- (GET) localhost:3001/api/tags/1
- (POST) http://localhost:3001/api/tags
    - json: {"tag_name": "Favorite Tag"}
- (DELETE) localhost:3001/api/tags/2
- (PUT) http://localhost:3001/api/tags/9
    - json: {"tag_name": "Updated to my Favorite Tag"}



## Technologies Used
* Node.js
* Express.js
* Sequelize
* MySQL
* Dotenv