# KatalonStudioProject
Assignments

Automation Engineer Technical Assignment

Introduction:
This assignment is divided into three parts namely:
1. REST API Automation Testing
2. Mobile Application Automation Testing
3. Performance Testing
Reading/Installation Material:
a. REST API : (to be used in Assignment 1)
https://drive.google.com/file/d/1A22qdYG8YO8GBDJmhdCNzknFCCKEwcGE
/view?usp=sharing
b. KATALON STUDIO: (to be used in Assignment 1)
https://docs.katalon.com
c. REST ASSURED :(to be used in Assignment 1)
http://rest-assured.io/
d. TESTNG : (to be used in Assignment 1)
https://testng.orgCopy of Gram Power Automation Engineer
Assignment/doc/index.html


Assignment 1:
The first task at hand is to automate the REST API’s testing using
either of the two different approaches :
A. Katalon Studio ( IDE ) :
Setup Katalon Studio on your machine by following guidelines on
https://www.katalon.com/download/ About api testing :
https://docs.katalon.com/katalon-studio/tutorials/create_first_
api_test_katalon_studio.html
b. Using TestNg, RestAssured and Java
Setup TestNg,RestAssured ,Java and eclipse(or whichever IDE you
prefer) by following guidelines of respective softwares.
REST API’s endpoints:
# Route Method

# Route Method

Type Start route Description

1   /users          GET      JSON      https://reqres.in/api       Get some users data with pagination

2   /users/{id}     GET      JSON      https://reqres.in/api       Get a single user data

3   /users          POST     JSON      https://reqres.in/api       Create new record in database

4   /users/{id}     PUT      JSON      https://reqres.in/api       Update an user record

5   /users/{id}     DELETE   JSON      https://reqres.in/api       Delete an user record


Automate and test all of the above REST API’s using any of the
approaches with these scenarios as test cases:
1. Scenario 1 :
Use API route #3 to create a new record with the following
parameters:
{
"name": "morpheus",
"job": "leader"
}
The response of this request will be :
{
"name": "morpheus",
"job": "leader",
"id": "229",
"createdAt": "2020-03-30T12:05:15.687Z"
}
Note: “id” key will be different every time you request.

Test Cases In Scenario 1:
a. Verify that after POST request the status code returned
is 201.
b. Verify the name,job returned in response is the same that
you entered while creating the record.
c. Also Capture the “id” key of the returned response and
perform a GET request at route #2 with this id and verify
that you received the same response that you entered while
creating the record by comparing the name and job keys.

2. Scenario 2 :
Update an user record by using route #4 with the following
request body (provide “id” key captured in above to the route):
{
"name": "morpheus",
"job": "zion resident"
}

Test Cases in Scenario 2:

a. Verify that the response received after performing an
update request is the same as above.
b. Also, using the route #2, verify that the updated record
is persisted with the same values.

3. Scenario 3 :
Delete a user record with the “id” key generated above using
route #5.
Test Cases in Scenario 3:
a. Verify that after performing the request , you receive
204 as HTTP Status Code.

NOTE: Test cases should be run using TestNg as a framework.
