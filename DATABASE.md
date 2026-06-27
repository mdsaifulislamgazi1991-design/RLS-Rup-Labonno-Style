# RLS Database Design

## Users Table
- id
- name
- email
- password
- role (admin / vendor / customer)
- created_at
- updated_at

## Vendors Table
- id
- user_id
- shop_name
- shop_description
- logo
- status

## Categories Table
- id
- name
- slug
- created_at

## Products Table
- id
- vendor_id
- category_id
- name
- description
- price
- stock
- image
- status
- created_at

## Carts Table
- id
- user_id
- product_id
- quantity

## Orders Table
- id
- user_id
- total_price
- status (pending, processing, shipped, delivered)
- created_at

## Order Items Table
- id
- order_id
- product_id
- quantity
- price

## Payments Table
- id
- order_id
- payment_method (bkash, nagad, sslcommerz)
- payment_status
- transaction_id
