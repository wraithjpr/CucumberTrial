# Cucumber and Gherkin Trial

My experiments with Cucumber and Gherkin. See Cucumber at [cucumber.io](https://cucumber.io/) and on GitHub at [github.com/cucumber/cucumber](https://github.com/cucumber/cucumber).
Cucumber for JavaScript is on GitHub at [github.com/cucumber/cucumber-js](https://github.com/cucumber/cucumber-js).

This trial works it's way through the JavaScript tutorial at [docs.cucumber.io/guides/10-minute-tutorial/](http://docs.cucumber.io/guides/10-minute-tutorial/).

The project structure is adapted from Andras Toth's [Codeship post](https://blog.codeship.com/advanced-node-js-project-structure-tutorial/): _Toth, Andras; Advanced Node.js Project Structure Tutorial; 2018-04-03_.

## To Dos
- [ ] How to treat acceptance tests in Cucumber vs unit tests in Mocha?
- [ ] How to incorporate into a WebPack workflow?

I have adopted Toth's approach for unit tests. Unit test files are placed next to the tested modules using the naming convention, `<module_name>.spec.js`. Tests live together with the tested modules, keeping them in sync, because it would be more difficult and so less convenient to find and maintain the tests and the corresponding functionality when the test files are completely separated from the business logic. A separated `/test` folder holds all the additional test setup and utilities not used by the application itself.

```text
.
|-- config
|-- dist
|   |-- app.bundle.js
|   `-- index.html
|
|-- features
|   |-- step_definitions
|	`-- stepdefs.js
|
|-- .git
|-- node_modules
|-- src
|   |-- api
|   |-- www
|       |-- index.html
|       |-- index.js
|       `-- style.css
|
|-- test
|   `-- setup.js
|
|-- cucumber.js
|-- .eslintrc.js
|-- .gitignore
|-- LICENSE.txt
|-- package.json
|-- package-lock.json
|-- README.md
|-- server.js
`-- webpack.config.js

```

