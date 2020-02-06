## This is my activity in database 2 the nodepg and the important codes/snippets are the following:
npm install --save dotenv
use .env
add require('dotenv').config() in index.js above const { Pool } = require('pg');
run your program using node index.js

## In case of error ERR_SOCKET_BAD_PORT, here are the steps that you need to consider:
Remove backticks in port: ${process.env.DB_PORT} 
 ## Problem: $ node index.js (node:9112) DeprecationWarning: Implicit disabling of certificate verification is deprecated and will be removed in pg 8. Specify rejectUnauthorized: true to require a valid CA or rejectUnauthorized: false to explicitly opt out of MITM protection.
1. change the sll: true,
    to
    ssl: {
        rejectUnauthorized: false,
    }