---
title: API DOCS
---
# OFFICIAL API DOCUMENTATION

:::warning

PRODUCT IS STILL IN BETA. API'S ARE SUBJECT TO CHANGE

:::

## Table of Contents

[[toc]]

## Base URL

### Development URL

```http
http://localhost:3333/v1/api
```

### Production URL

```http
https://api.localmerch.in/v1/api
```

## Route /admin/

### Business

#### Get all businesses

```http
GET /business
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

#### Response

```json
[
	{
		"pan": true,
		"orders": [],
		"active": true,
		"m_orders": [],
		"revenue": [],
		"a_revenue": 0,
		"a_orders": 0,
		"customers": 0,
		"createdAt": 1629268465,
		"_id": "611ca9f15474dc18ecdc3f09",
		"uid": "murimuri",
		"name": "Oishik",
		"email": "oishik@bantu.in",
		"username": "murimann",
		"c_email": "oishik@bantu.in",
		"brand": "muricompany",
		"phone": "+915555522222",
		"category": "food",
		"desc": "khastamuri",
		"insta": "@oishik7",
		"link": "google.com",
		"zip": "700078",
		"cp": "https://unsplash.it/512/512",
		"dp": "https://unsplash.it/1920/300",
		"__v": 0
	},
	{
		"pan": true,
		"orders": [],
		"active": true,
		"m_orders": [],
		"revenue": [],
		"a_revenue": 0,
		"a_orders": 0,
		"customers": 0,
		"createdAt": 1629269727,
		"_id": "611caf130e517a5694109ab7",
		"uid": "oishikid",
		"name": "Bhanu",
		"email": "oishik@bantu.com",
		"username": "murgiman",
		"c_email": "oishik@bantu.in",
		"brand": "muricompany",
		"phone": "+915555522222",
		"category": "food",
		"desc": "motamuri",
		"insta": "@bhanunu",
		"link": "google.com",
		"zip": "700075",
		"cp": "https://unsplash.it/512/512",
		"dp": "https://unsplash.it/1920/300",
		"__v": 0
	}
]
```

#### Get a business by id

```http

  GET /business

```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Request

```json
{
	"id": "611caf130e517a5694109ab7"
}
```

#### Create a business

```http

POST /business

```

| Parameter       | Type     | Description                   |
| :-------------- | :------- | :---------------------------- |
| `authorization` | `string` | _Required_. Your API key      |
| `uid`           | `string` | _Required_. firebase uid      |
| `name`          | `string` | _Required_. business name     |
| `email`         | `string` | _Required_. business email    |
| `username`      | `string` | _Required_. business username |
| `c_email`       | `string` | _Required_. email for client  |
| `brand`         | `string` | _Required_. brand name        |
| `phone`         | `string` | _Required_. phone             |
| `category`      | `string` | _Required_. category          |
| `desc`          | `string` | _Required_. description       |
| `insta`         | `string` | _Required_. insta link        |
| `link`          | `string` | _Required_. other links       |
| `zip`           | `string` | _Required_. pin code          |
| `cp`            | `string` | _Required_. cover pic         |
| `dp`            | `string` | _Required_. display pic       |

#### Update a business

```http
PUT /business
```

| Parameter       | Type      | Description                   |
| :-------------- | :-------- | :---------------------------- |
| `authorization` | `string`  | _Required_. Your API key      |
| `uid`           | `string`  | _Required_. firebase uid      |
| `name`          | `string`  | _Required_. business name     |
| `username`      | `string`  | _Required_. business username |
| `phone`         | `string`  | _Required_. phone             |
| `category`      | `string`  | _Required_. category          |
| `desc`          | `string`  | _Required_. description       |
| `insta`         | `string`  | _Required_. insta link        |
| `link`          | `string`  | _Required_. other links       |
| `active`        | `boolean` | _Required_. active            |
| `pan`           | `string`  | _Required_. pan               |
| `zip`           | `string`  | _Required_. pin code          |

#### Delete a business

```http
DELETE /business
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

### Products

#### Get all products of a business by business id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

#### Get individual product by id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Create a new product

```http
POST /products
```

| Parameter       | Type      | Description               |
| :-------------- | :-------- | :------------------------ |
| `authorization` | `string`  | _Required_. Your API key  |
| `uid`           | `string`  | _Required_. firebase uid  |
| `name`          | `string`  | _Required_. business name |
| `desc`          | `string`  | _Required_. description   |
| `price`         | `string`  | _Required_. product price |
| `owner_id`      | `string`  | _Required_. other links   |
| `pics`          | `boolean` | _Required_. picture link  |
| `size`          | `string`  | _Required_. size          |
| `colour`        | `string`  | _Required_. colour        |
| `limit`         | `string`  | _Required_. limit         |

#### Update a product

```http
PUT /products
```

| Parameter       | Type      | Description               |
| :-------------- | :-------- | :------------------------ |
| `authorization` | `string`  | _Required_. Your API key  |
| `uid`           | `string`  | _Required_. firebase uid  |
| `name`          | `string`  | _Required_. business name |
| `desc`          | `string`  | _Required_. description   |
| `price`         | `number`  | _Required_. product price |
| `limit`         | `number`  | _Required_. other links   |
| `pics`          | `boolean` | _Required_. picture link  |
| `size`          | `string`  | _Required_. size          |
| `colour`        | `string`  | _Required_. colour        |
| `active`        | `boolean` | _Required_. active        |

#### Delete a product

```http
DELETE /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

### Orders

#### Get all orders

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

#### Get order by id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |

#### Get all orders of a business by business id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Get all orders of a customer by customer id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### create a new order

```http
POST /orders
```

| Parameter       | Type      | Description                    |
| :-------------- | :-------- | :----------------------------- |
| `authorization` | `string`  | _Required_. Your API key       |
| `uid`           | `string`  | _Required_. firebase uid       |
| `id`            | `string`  | _Required_. business id        |
| `name`          | `string`  | _Required_. business name      |
| `email`         | `string`  | _Required_. email              |
| `shipping`      | `string`  | _Required_. shipping details   |
| `brand`         | `number`  | _Required_. brand name         |
| `payment`       | `boolean` | _Required_. payment details    |
| `order`         | `string`  | _Required_. order details      |
| `additional`    | `string`  | _Required_. additional details |

#### Update an order status

```http
PUT /orders
```

| Parameter       | Type      | Description              |
| :-------------- | :-------- | :----------------------- |
| `authorization` | `string`  | _Required_. Your API key |
| `id`            | `string`  | _Required_. id           |
| `active`        | `boolean` | _Required_. active       |

### Customers

#### Get all customers or a specific customer by id

```http
GET /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Create a new customer

```http
POST /customers
```

| Parameter       | Type     | Description                  |
| :-------------- | :------- | :--------------------------- |
| `authorization` | `string` | _Required_. Your API key     |
| `uid`           | `string` | _Required_. firebase uid     |
| `name`          | `string` | _Required_. business name    |
| `email`         | `string` | _Required_. email            |
| `shipping`      | `string` | _Required_. shipping details |

#### Update a customer

```http
PUT /customers
```

| Parameter       | Type     | Description                  |
| :-------------- | :------- | :--------------------------- |
| `authorization` | `string` | _Required_. Your API key     |
| `uid`           | `string` | _Required_. firebase uid     |
| `name`          | `string` | _Required_. business name    |
| `email`         | `string` | _Required_. email            |
| `shipping`      | `string` | _Required_. shipping details |

#### Delete a customer

```http
DELETE /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

## Route /business/

### Business

#### create a new business or register a new user

```http
GET /business
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Create a new business or register a new user

```http
POST /business
```

| Parameter       | Type     | Description                   |
| :-------------- | :------- | :---------------------------- |
| `authorization` | `string` | _Required_. Your API key      |
| `uid`           | `string` | _Required_. firebase uid      |
| `name`          | `string` | _Required_. business name     |
| `email`         | `string` | _Required_. business email    |
| `username`      | `string` | _Required_. business username |
| `c_email`       | `string` | _Required_. email for client  |
| `brand`         | `string` | _Required_. brand name        |
| `phone`         | `string` | _Required_. phone             |
| `category`      | `string` | _Required_. category          |
| `desc`          | `string` | _Required_. category          |
| `insta`         | `string` | _Required_. insta link        |
| `link`          | `string` | _Required_. other links       |
| `zip`           | `string` | _Required_. pin code          |
| `cp`            | `string` | _Required_. cover pic         |
| `dp`            | `string` | _Required_. display pic       |

#### Update a business

```http
PUT /business
```

| Parameter       | Type      | Description                   |
| :-------------- | :-------- | :---------------------------- |
| `authorization` | `string`  | _Required_. Your API key      |
| `uid`           | `string`  | _Required_. firebase uid      |
| `name`          | `string`  | _Required_. business name     |
| `username`      | `string`  | _Required_. business username |
| `phone`         | `string`  | _Required_. phone             |
| `category`      | `string`  | _Required_. category          |
| `desc`          | `string`  | _Required_. description       |
| `insta`         | `string`  | _Required_. insta link        |
| `link`          | `string`  | _Required_. other links       |
| `active`        | `boolean` | _Required_. status            |
| `pan`           | `string`  | _Required_. pan               |
| `zip`           | `string`  | _Required_. pin code          |

#### Delete a business

```http
DELETE /business
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

### Products

#### Get all products of a business by business id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

#### Get individual product by id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Create a new product

```http
POST /products
```

| Parameter       | Type     | Description                      |
| :-------------- | :------- | :------------------------------- |
| `authorization` | `string` | _Required_. Your API key         |
| `uid`           | `string` | _Required_. firebase uid         |
| `name`          | `string` | _Required_. business name        |
| `desc`          | `string` | _Required_. business description |
| `price`         | `number` | _Required_. item price           |
| `owner_id`      | `string` | _Required_. owner id             |
| `pics`          | `string` | _Required_. picture link         |
| `limit`         | `number` | _Required_. item limit           |

#### Update a product

```http
PUT /products
```

| Parameter       | Type     | Description                      |
| :-------------- | :------- | :------------------------------- |
| `authorization` | `string` | _Required_. Your API key         |
| `uid`           | `string` | _Required_. firebase uid         |
| `name`          | `string` | _Required_. business name        |
| `desc`          | `string` | _Required_. business description |
| `price`         | `number` | _Required_. item price           |
| `pics`          | `string` | _Required_. picture link         |
| `limit`         | `number` | _Required_. item limit           |

#### Delete a product

```http
DELETE /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

### Orders

#### Get all orders

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

#### Get order by id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. Business id  |

#### Get all orders of a business by business id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |
| `business_id`   | `string` | _Required_. business id  |

#### Get all orders of a customer by customer id

```http
GET /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |
| `customer_id`   | `string` | _Required_. customer id  |

#### Update an order status

```http
PUT /orders
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |

## Route /client/

### Business

#### Get a list of all businesses

```http
GET /business
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |

### Products

#### Get all products of a business by business id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |
| `business_id`   | `string` | _Required_. business id  |

#### Get individual product by id

```http
GET /products
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |

### Customers

#### Get a specific customer by id or login

```http
GET /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |

#### Create a new customer or register a new customer

```http
POST /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |
| `email`         | `string` | _Required_. email        |
| `name`          | `string` | _Required_. name         |
| `uid`           | `string` | _Required_. uid          |

#### Update a customer

```http
PUT /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |
| `email`         | `string` | _Required_. email        |
| `name`          | `string` | _Required_. name         |
| `shipping`      | `string` | _Required_. shipping     |

### Orders

#### Get all orders of a customer by id

```http
GET /customers
```

| Parameter       | Type     | Description              |
| :-------------- | :------- | :----------------------- |
| `authorization` | `string` | _Required_. Your API key |
| `id`            | `string` | _Required_. id           |

