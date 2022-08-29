# Design

## Overall Architecture

This app uses a client-server model. The client is responsible for parsing the input file, talking to the backend to get the change amounts, and producing the output file. The backend is responsible for keeping track of what currencies and coin denominations are available, handling requests from the frontend, and calculating the change amounts.

I chose this model because I was thinking of the larger system that this code might be a part of. By separating the logic for actually calculating change amounts into a REST API, it can be reused by other clients in other scenarios. For example, one might imagine a point-of-sale system that calls this API. In this case, the cashier only has to enter the amount paid (assuming the amount owed is automatically tallied as they scan items, and the currency is pre-set on their system). Then the change that they need to give might be displayed as a GUI, perhaps with images of the coins needed to make it easy for them. To make a system like this would require a new frontend, but could reuse the backend entirely.

## Backend

## Frontend