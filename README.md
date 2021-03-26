# Exercise using Postman and Newman to test Todoist REST API

## How to run
1. download the collection and the environment files
2. open your commmand line and go to the directory you saved the downloaded files
3. run the following command
> `newman run todoist_.postman_collection.json --environment dev.postman_environment.json -r html`

## Check results
A new folder named 'newman' is created, inside you'll find the output of the HTML reporter

## How to manage secrets
One possible way could be to setup a Jenkins job in which you can create a Credential in which to store the APIKEY in order to avoid keeping sensitive data in a code repository
Then you can refer to the stored Credential and pass it as a variable to the step where newman is executed using -–global-var or --env-var 

## Outro
I had lots of fun doing this exercise with Postman. Creation of requests and usage of variables was not that much of a problem; but I had to make some google searches to find out some stuff inside the test functions. Luckily Postman is very friendly and provides a lot of help, almost like an IDE suggesting functions and autocompleting. That came in handy.

I thought I would have a bit of trouble using Newman since it was something completely new and I hadn't use it before. But again, the documentation is very friendly; I was able to find everything kinda quick.

