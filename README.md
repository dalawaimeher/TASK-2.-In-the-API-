# node-mongo-registration-login-api

NodeJS + MongoDB API for User Management, Authentication and Registration

For documentation and instructions check out http://jasonwatmore.com/post/2018/06/14/nodejs-mongodb-simple-api-for-authentication-registration-and-user-management



My Explanation  


SUB-TASK    1.    Change the login API to also record the login/logout of a user with the timestamp and the client IP 
 - for this i have added details in model so when ever user logs in we can capture all req data n storee.

SUB-TASK    2.    Implement a new API (GET /audit) that will retrieve all login/logout of users with the timestamp and the client IP 
       a. If a user is not having the AUDITOR role the /audit API should return an HTTP 401 response
    - for IP we can use ip node module for storing format in db
    - i have written /audit api by taking username as input n validating with "AUDITOR"role which we are capturin at time of login  n then sending all users data as response
