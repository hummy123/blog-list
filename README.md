# Blog List API

A REST API made using Node.js that handles requests to create, update and delete blogs hosted on a MongoDB database.

Token authentication, as well as user login is implemented with the help of jsonwebtoken.

A number of integration tests have been written for the API with Jest.  

## Setting up

1. Install the project dependencies with the usual ```npm install```.
2. Define environment variables ```MONGODB_URI```, ```PORT``` and ```SECRET```.
3. Start the API with ```npm start```.

## Usage

Once the API has started, HTTP ```GET``` requests can be made through a browser through the routes defined in the ```controllers``` folder.

Other HTTP requests, such as ```POST```, ```PUT``` and ```DELETE``` can be made via an IDE such as WebStorm, Visual Studio Code or a tool built for this purpose such as Postman.

In order to perform modifications on blogs, a user must submit an authentication token along with the request.

This can be done via a ```POST``` request to ```/api/users```  (creating a user) and then another ```POST``` request to ```/api/login```.

Doing the above will make the server respond with an authentication token, which can be sent with a ```POST```, ```PUT``` or ```DELETE``` request in the authorization header using a format such as ```Authorization: bearer [token]```.

## Running tests

The tests can be run by entering ```npm run test```.
