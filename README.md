## Project React Shopify

A mini project ecommerce where authenticate user can fetch the products, see their details and add the products to cart.

## Configuration

Create .env file in root directory and fill in the following details:

```
PORT=5000
MONGO_URI='YOUR DB URI'

##For JWT Authentication
JWT_SECRET='YOUR SECRET KEY'
JWT_EXPIRE='10min'

NODE_ENV='development/production'

##For Password Reset
EMAIL_SERVICE=''
EMAIL_HOST=''
EMAIL_PORT=''
EMAIL_USERNAME=''
EMAIL_PASSWORD=''
EMAIL_FROM=''
```

## Quick Start

```javascript
//Install dependencies for server and client
yarn install && yarn client-install

//Run client and server with concurrently
yarn dev

// Server runs on http://localhost:5000 and client on http://localhost:3000

```

### Database Structure: (Table: columns)

    1. categories: _id, name, createdAt, updatedAt;
    2. orders:  _id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
    3. products: _id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
    4. users: _id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt

### App Description:

    1. user can view all products
    2. user can view single product
    3. user can search products and view products by category and price range
    4. user can add to cart checkout products using credit card info
    5. user can register & sign in
    6. admin can create, edit, update & delete products
    7. admin can create categories
    8. admin can view ordered products
    9. admin can change the status of a product (processing, shipped, delivered, etc.)
