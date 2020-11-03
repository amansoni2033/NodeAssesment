# NodeAssesment

Blogging App:-

This is a blogging application developed by using Node.js, Express,PostgreSql and sequelize.
The main purpose of this project is execute basic http method like get(), post(), delete(), put() http methods.



You can follow the instructions for building this blog application here:

Step 1:-

Things you must do first:
a) Install Node
b) Install PostgreSql
c) Install Git Bash

Step 2:- 

After first step we will install required javascript library and other library using following command.

 1)npm install express
 2)npm install jsonwebtoken
 3)npm install md5
 4)npm install passport
 5)npm install passport-jwt
 6)npm install pg
 7)npm install pg-hstore
 8)npm install sequelize

 Step 3:-

 After installation of all library and project metadata or description the package.json files look like this.

 {
  "name": "nodeassesment",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node ./src/index.js"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/amansoni2033/NodeAssesment.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/amansoni2033/NodeAssesment/issues"
  },
  "homepage": "https://github.com/amansoni2033/NodeAssesment#readme",
  "dependencies": {
    "express": "^4.17.1",
    "jsonwebtoken": "^8.5.1",
    "md5": "^2.3.0",
    "passport": "^0.4.1",
    "passport-jwt": "^4.0.0",
    "pg": "^8.4.2",
    "pg-hstore": "^2.3.3",
    "sequelize": "^6.3.5"
  }
}

Step 4:-

  After this I made the github repository of name NodeAssesment with including .gitignore and ReadMe files.
  and Cloned on main NodeJsAssesment directory by using following command.

  $ git clone git@github.com:amansoni2033/NodeAssesment.git


Step 5:

  After all we will make a src folder and make a main index.js file. And in this main index.js file we will import express library by using this following statement.

  const express = require("express"); 
  const app = express();

And we will also import all middleware.

app.use(express.json());
app.use(express.urlencoded());
app.use(passport.initialize());


Step 6:

And after we will import all requirement library in this index.js file.

const { request } = require("express");
const express = require("express");
const passport = require("passport");
const movieController = require("./controller/blog");
const userController = require("./controller/user");
const authController = require("./controller/auth");
const db = require("./database/index");
const { SIGNING_KEY, sanitizeUser } = require("./utility");

const JwtStrategy = require("passport-jwt").Strategy,
ExtractJwt = require("passport-jwt").ExtractJwt;


Step 7:
- Build a blogging app where  user can create blogs , read blogs. essenntially it would be set of end points.
    - `post /auth/signup`  registers the user
    - `post /AUTH/LOGIN` login using jwt
    - `post blogs/`  create a blog for logged in user
    - `get /blogs`  get list of blogs for user from all the other users
    - `get /blogs/id`  get specific blog for user
    - `put /blogs/id`  user can update it's own blog
    - `delete /blogs/id` user can delete his own blog


  














 
