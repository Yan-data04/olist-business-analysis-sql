# Dataset Explaination

## Olist Seller Dataset
**Description:** Stores every seller on the Olist marketplace. Might be useful for seller performance and geographic seller distribution analysis.\
\
**Columns:** 
1. seller_id
2. seller_zipcode
3. seller_city
4. seller_state

## Olist Customer Dataset
**Description:** Stores every buyer. Each row is a customer for one order.\
\
**Columns:** 
1. customer_id
2. customer_unique_id
3. customer_zipcode
4. customer_state
5. customer_city

## Olist Orders Items Dataset
**Description:** Stores every order placed on Olist. Include with the full timestamp lifecycle: purchase → approved → handed to carrier → delivered to customer → estimated delivery date. This table alone answer almost every delivery/logistics question (late delivery %, delivery time, etc.) since it's the only place with dates.\
\
**Columns:** 
1. order_id
2. customer_id
3. order_status
4. order_approved_at
5. order_purchase_timestamp
6. order_delivered_carrier_date
7. order_delivered_cust_date
8. order_estimated_delivery_date

## Olist Orders Dataset
**Description:**  Stores every every items placed in an order. Can be used to calculate revenue.\
\
**Columns:** 
1. order_id
2. order_item
3. product_id
4. seller_id
5. shipping_limit_date
6. price
7. freight_value

## Olist Orders Payments
**Description:**  How the order was paid\
\
**Columns:** 
1. order_id
2. payment_type
3. payment_value
4. payment_sequential
5. payment_installments

## Olist Products Dataset
**Description:**  The catalog. Dataset where they store all the product category and description.\
\
**Columns:** 
1. product_id
2. product_cat_name
3. product_weight_g
4. product_name_length
5. product_desc_length
6. product_length_cm
7. product_photos_qty
8. product_height_cm
9. product_width_cm

## Olist Order Reviews Dataset
**Description:**  Post-purchase satisfaction. Store order reviews. \
\
**Columns:** 
1. review_id
2. order_id
3. review_score
4. review_comment_msg
5. review_creation_date
6. review_comment_title
7. review_answer_timestamp

## Olist Geolocation Dataset
**Description:** Zip-code-prefix → lat/lng lookup, used to plot customers/sellers on a map. Messy join, being trated as optional or supplementary table in the project.\
\
**Columns:** 
1. geolocation_zipcode
2. geolocation_lat
3. geolocation_lng
4. grolocation_city
5. geolocation_state

## Product_category_name_translation
**Description:** A tiny lookup table (~70 rows) mapping the Portuguese category names in products to English.
