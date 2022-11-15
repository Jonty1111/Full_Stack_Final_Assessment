<b> Services and Their Port Nos: </b>

    Eureka Server : 8761
    Token Sevice : 6080
    Admin Service : 6081
    Consumer Service : 6082
    ShopMgmt Service : 6083
    Shop Service : 6084

<b>Screenshot of Services in Eureka: </b>
![image](https://user-images.githubusercontent.com/112845359/201834084-9fe1fada-bb1a-46ef-8d90-80deb4e680fe.png)




<b>Postman Link: </b>

    https://www.getpostman.com/collections/deafeb5569951ea15b3f


<b>API END-POINTS:</b>


ADMIN SERVICES:

    1.1)SIGNUP:

    Method: POST
    Endpoint: http://localhost:6081/user/signup
    Payload:
    { "username" : "jonty", "password" : "1234",
    "password_confirm" : "1234", "email": "jonty@gamil.com" }




    1.2) LOGIN:

    Method: POST
    Endpoint: http://localhost:6081/user/login
    Payload:
    { "username" : "jonty", "password": "1234" }



    1.3) GET-USERS:

    Method: GET
    Endpoint: http://localhost:6081/user/get-users




SHOP SERVICES:

    2.1) GET-PRODUCTS:

    Method: GET
    Endpoint: http://localhost:6084/shop/products



    2.2) GET-PRODUCTS-BY-FIELD:

    Method: POST
    Endpoint: http://localhost:6084/shop/products
    Payload:
    { "description": "19 KG" }



    2.3) GET-CATEGORIES:

    Method: GET
    Endpoint: http://localhost:6084/shop/categories



    2.4) GET-CATEGORIES-BY-FIELD:

    Method: POST
    Endpoint: http://localhost:6084/shop/categories
    Payload:
    { "description": "Clothes" }




CONSUMER SERVICES: (TOKEN REQUIRED)

3.1) CATEGORIES:

    3.1.1) GET categories:
    Method: GET
    Endpoint: http://localhost:6082/consumer/shop-management/categories


    3.1.2) ADD category
    Method: POST
    Endpoint: http://localhost:6082/consumer/shop-management/add-category
    PAYLOAD :
    { "name": "Automobiles", "description": "Auto Related" }


    3.1.3) UPDATE category by ID

    Method: POST
    Endpoint: http://localhost:6082/consumer/shop-management/update-category-by-id/{id}
    PAYLOAD :
    { "name" : "Clothing" }


    3.1.4) DELETE category by ID
    Method: DELETE
    Endpoint: http://localhost:6082/consumer/shop-management/delete-category-by-id/{id}


3.2) PRODUCTS:


    3.2.1) GET Products
    Method: GET
    Endpoint: http://localhost:6082/consumer/shop-management/products


    3.2.2) ADD PRODUCT
    Method: POST
    Endpoint: http://localhost:6082/consumer/shop-management/add-product
    PAYLOAD :
    { "name": "Nike Shirt", "price" : "6000", "description": "RED M" }


    3.2.3) LINK PRODUCT WITH CATEGORY
    METHOD: PUT
    Endpoint: http://localhost:6082/consumer/shop-management/product-with-category/{product_id}/{category_id}


    3.2.4) UPDATE PRODUCT by ID
    Method: POST
    Endpoint: http://localhost:6082/consumer/shop-management/update-product-by-id/{id}
    PAYLOAD :
    { "price" : 12000 }
    allowed fields: description OR name OR id OR price


    3.2.5) DELETE PRODUCT by ID
    Method: DELETE
    Endpoint: http://localhost:6082/consumer/shop-management/delete-product-by-id/{id}
