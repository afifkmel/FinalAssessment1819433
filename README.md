### Muhammad 'Afif Akmal bin Adnan 1819433

# GadgetStore

## Introduction

Gadget Store is a web application for the inventory management system of a gadget business store. It provides
a wide variety of products including different parts and accessories to customers. 
A gadget store would include products like smartphones, cases, powerbanks etc. 

## Objectives of Enhancement
- to improve the original web app development project before
- to provide web app with secure features
- to prevent security vulnerabilities against threats such as unauthorized access and modification to the web app

## Web Application Security Enhancement

### i. Input Validation
- Whitelist Validation. Any input that the user key in that does not match an explicit allow-list or allow-pattern is rejected.
- For example; email validation in login page, character validation in the adding and editing data form, etc

### ii. Authentication
- Just like most other web apps, GadgetStore encourages strong password to safeguard users account.
- This web apps only can be access by staffs which their login details already key in in the database(seeders)
- There is no registration available through the web app

### iii. Authorization
- Since GadgetStore is an inventory management system, the only users in this web app is the staffs or admins. The authorized resources that staffs or admins are able to access are to add products, editing the products data, update or delete the products.
- For example, staffs have access to add new stocks of smartphone
- However, to add or remove new staff/s, it only can be done by the developer

### iv. XSS and CSRF Prevention
- Since GadgetStore is develope with laravel, CSRF attacks rarely to occur.
- This is because, Laravel already has a built in features which are CSRF protection
- However, Laravel apps are vulnerable to XSS attacks.
- So, to prevent it, I rewrite the code by replacing the standard PHP code with a blade function.
- This is because, blade code uses the {{ }} echo statement to escape the value of the parameter. This causes the value to be rendered as plain text all the time.
- User can insert <iframe>..</iframe> or any malicious script into any textfield but nothing happen. 
- For example, in the form to add products. Nothing will happen, but it will only add the products with the script as words.
- Types of defenses used by Laravel is sanitizing input for checking, filtering, and cleaning data inputs from app users. With sanitization in place, these attacks(XSS & CSRF) can be prevented

### v. Database Security Principles
- By using Laravel, there is some of the security features already built in to the framework raw queries can be avoided as much as users can.
- With the help of the Eloquent ORM, the app can reads and writes data to an SQL database without writing a single raw SQL query.

### vi. File Security Principles
- 





- display gadgets in categories, price and information
- add to cart function
- calculation of the cart 
- payment page 

## Navigations & Routings
![navviiii](https://user-images.githubusercontent.com/55817844/174639453-ae54da19-d9bc-4c2d-88c9-2eee3f9f73b2.PNG)

## Widgets
![naviiii widget](https://user-images.githubusercontent.com/55817844/174641628-0666f510-d161-433b-bfe5-98c0f8d3b06c.png)

## Sequence Diagram
![111111](https://user-images.githubusercontent.com/55817844/174641771-7c8aa851-398c-4a2c-9153-314c17f92e9c.PNG)
![22222](https://user-images.githubusercontent.com/55817844/174641793-7dd355ca-cc7f-49b8-bb37-fef061b25ce6.PNG)

## References
-Flutter Documentation
https://flutter.dev/?gclid=CjwKCAjwtcCVBhA0EiwAT1fY775rQrBDqIPY7A-KMB24vs8Ren-A-onFJudfYjA6LMllX8_6Rn5T0hoCiYgQAvD_BwE&gclsrc=aw.ds

-Diagram
https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-sequence-diagram/
