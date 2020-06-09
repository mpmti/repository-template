# Workflow for automated tests with Angular

Automating test for Angular with a workflow requires the actual workflow (c.f. `.github/workflows/run-tests.yml`), changes to the standard Karma and Protractor configurations and also some additional dependencies.


Karma and Protractor must be configured such that they test with a headless browser, or else the github actions can not execute the tests (c.f. `karma-ci.conf.js` and `e2e/protractor-ci.conf.js` ).
They use [Puppeteer](https://www.npmjs.com/package/puppeteer) for that headless browser stuff.


There are also some added scripts (`autotest` and `autoe2e`) in the package.json to simplify the actual workflow.

---

# Angulartest

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.6.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
