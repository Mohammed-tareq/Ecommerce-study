# E-commerce-study

User => product => cart => checkout => payment => order

User Schema
    name
    email
    password
    country
    governorate
    city
    phone
    image

Product Schema
    name
    small description
    description
    price
    sku
    qty
    images
    discount
    category

Cart Schema
    user_id

Cart Item Schema
    cart_id
    product_id
    qty
    product_price
    total_price

Order Schema
    user_id
   transaction_id
    total_price
    status

order item schema
    order_id
    product_id
    qty
    product_price
    total_price

transactions schema
    order_id
    payment_method
    payment_status
    invoice_id


User Stroy 

first step user shouldn't be able to register and login to the system to see all products.
user can show all product with end point /products
user can login with end point /login
user can register with end point /register


***user can't add to cart if not login,

user can add to cart if login  /add-to-cart
    if the product is already in the cart so the item is increment by one for this product
user can show cart items with end point /cart-items
user can remove cart item with end point /remove-from-cart/{cartItemId}
user can remove all items from cart with end point /remove-all-items-from-cart

user can checkout with end point /checkout
check cart not empty
create order for each cart item
user can pay for order with end point /pay
    if payment success update order status to paid
    if payment failed update order status to failed
user can show orders with end point /orders

