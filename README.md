# COMPSCI 326 Web Programming

## Exercise: Routing

**DUE: 4/6/2022 (by midnight)**

You are to write your program using [VSCode](https://code.visualstudio.com/). You can run your code using [Node.js](https://nodejs.org/en/) and the command line.

You may ask questions on Slack _#q-and-a-lecture_ but do not post code. You can post code in private messages sent to all the course staff.

This exercise uses the solution from **Exercise 12 CRUD #2** where we extended a CRUD-based HTTP server with a front-end UI. In this exercise, we are going to use the [ExpressJS](https://expressjs.com/) server-side web framework in place of the built-in Node.js [`http`](https://nodejs.org/api/http.html) library. As you will see, the ExpressJS framework is a lot more "expressive" than the built-in HTTP library. It allows us to write more concise code and is easier to read.

_It will be helpful to reference the server code examples covered in class to provide guidance on the implementation of this exercise. The template we provide also gives you significant direction._

## Setup

After you accept this exercise from Github Classroom, you will need to clone the repository to your local machine. After you clone the repository, you can open it up in VSCode and install the necessary dependencies in the Terminal from within the project directory. Run the following commands:

```bash
npm init
npm install --save express
npm install --save morgan
```

This will update your `package.json` file to include the ExpressJS framework and the Morgan logging library as well as install the dependencies in the `node_modules` directory. After installing the dependencies, you will need to add the following line to your `package.json` file under the entry for `"description"` to support ES6 module syntax in your server code:

```json
"type": "module"
```

After you have installed the dependencies and added the ES6 module support, you can run the following command to start the server:

```bash
node pcrud-fs.js
```

## Exercise 1: Completing the Express Server

The template we provide for you includes the setup of the ExpressJS server with a few of the routes completed. Your job is to complete the remaining routes. In particular, you are to do the following:

1. Add two new routes in the `pcrud-fs.js` file.:

   - `/update`: This route matches a `PUT` request to the `/update` path. It should pass the request body to the `updateCounter` function.

   - `/delete`: This route matches a `DELETE` request to the `/delete` path. It should pass the request body to the `deleteCounter` function.

     _You will find the creation of the ExpressJS server and routes we have provided towards the end of the file._

2. Complete the `updateCounter()` and `deleteCounter()` functions in the `pcrud-fs.js` file. You can use the other CRUD functions we implemented as guidance. It is important to note that you must call `response.json()` as the last line of the function. If you do not do this, you may encounter some subtle errors in the browser.

3. Complete the `updateCounter()` and `deleteCounter()` functions in the `client/crud.js` file. We made some slight changes to these RESTful calls to send JSON data to the server rather than use the query string. You can use the other CRUD functions we implemented as guidance. Note, we continue to use the query string for the `readCounter()` function. The reason we do this is because we are unable to use the request body with a `GET` request. If we wanted to use the request body, we would have to use the `POST` method. Although this technically violates the principles of RESTful APIs, it is a very common practice in the industry.

## Rubric

This exercise will be scored on the following criteria:

- 0: There is no submission or very little changes that are not recognized as a submission.
- 1: A minor attempt was made to complete the exercise. There were some changes that were recognized, but not enough to be considered a quality submission.
- 2: A moderate attempt was made to complete the exercise. There were some changes that were recognized, but parts of the submission were either not complete, not correct, and/or clear didn't demonstrate an understanding of the material and exercise.
- 3: A good attempt was made to complete the exercise. There were changes that were clearly recognized, and the submission was complete and mostly correct. Understanding of the material and exercise was clearly demonstrated.

## Submission

### GitHub Classroom

- To submit this exercise you must add, commit, and push your changes to GitHub by the assigned due date.

### Exercise Survey

- In order to receive credit for your submission, you must complete the corresponding exercise survey: [https://forms.gle/4DLcw7aCMBiVNMdy7](https://forms.gle/4DLcw7aCMBiVNMdy7)
