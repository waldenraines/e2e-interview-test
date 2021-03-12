# e2e Interview Test

## Setup

### 1. Install Cypress

[Follow these instructions to install Cypress.](https://on.cypress.io/guides/installing-and-running#section-installing)

### 2. Fork and Run Locally

[Fork](https://github.com/unchained-capital/e2e-interview-test#fork-destination-box) this project.

After forking this project in `Github`, run these commands:

```bash
## clone this repo locally
git clone https://github.com/<your-username>/e2e-interview-test.git

## cd into the cloned repo
cd e2e-interview-test

## install dependencies
npm install

## start the local webserver
npm start
```

The `npm start` script will spawn a webserver on port `8888` which hosts the TodoMVC app.

You can verify this by opening your browser and navigating to: [`http://localhost:8888`](http://localhost:8888)

You should see the TodoMVC app up and running and you can play around with it to get a sense of what it does.  Now we're ready to add to our test suite.

## Testing the Todo app:

We already have some tests written for this application.  We need you to add the 
following tests to `cypress/integration/app_spec.js`

Look in that file for `// TODO:` comments and add tests in those places.

## Running Tests

### Run the tests in headless mode
You can run the tests once in headless mode to check they are passing:

```bash
npm run test
```

###  Open cypress in dev mode

It can be useful to open cypress in dev mode in order to see what your tests are doing.

First quit out of the `npm start` above if you still have it running.

```bash
npm run dev
```

See also `package.json` for other ways to run the tests.

## Other Stuff

### Custom commands

This project also adds several custom commands in [cypress/support/commands.js](cypress/support/commands.js). They are useful to create one or more default todos from the tests.

```js
it('should append new items to the bottom of the list', function () {
  cy.createDefaultTodos().as('todos')
  // more test commands
})
```
