[![Status](https://img.shields.io/badge/status-NO%20COMMIT-blue.svg)]({{ cookiecutter.repo_url }})

# Status

A status badge will appear above after you make your first commit and the build completes. You can click into the badge to view information about your build. If you think the status is incorrect, check your build or please wait a couple minutes - it may still be building.

# Instructions

Complete the provided "order.html" to create a client and server integration for one-time purchases.

The server is already provided, so you will have to complete the client.

The client should achieve the following:

- an order button to execute the one-time purchase. Please use "checkout-button" as your button id
- a script that will create a post request to the server to create a checkout session.
    + server url: /create-checkout-session
    + parameters: quantity, img, amount, currency, name
- when an error is received, it should be shown in the "error-message" div
- when the post request is successful, it should return a session id. You will use this for your [checkout](https://stripe.com/docs/payments/checkout).
- your checkout upon success will trigger the server to redirect to the order_success page

## Dashboard Product
One time purchase product
* Product Name: {{ cookiecutter.product }}
* Currency: USD
* Amount: ${{ cookiecutter.amount }}

The repository includes the following files:
* `client/order.html`: complete this form to integrate with Checkout
* `client/order_success.html`: the application should redirect here when Checkout is successful
* `/img/cupcake.jpg`: use this image for your product

## how to run the server
1. Install [pipenv](https://pypi.org/project/pipenv/)
2. Run `pip install --user --upgrade pipenv` to get the latest pipenv version.
3. Run `pipenv --python 3.7`
4. Run `pipenv install`
5. Run `cp .env.example .env`
6. update .env with your keys. Domain should be your server url
7. Run `pipenv shell`
8. Run python app.py
9. access your app (http://127.0.0.1:5000/)

## how to run test
1. Run `pipenv shell`
2. Run python test.py
