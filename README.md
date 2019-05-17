# Cypress-CircleCI

[![CircleCI](https://circleci.com/gh/YOU54F/cypress-circleci/tree/master.svg?style=svg)](https://circleci.com/gh/YOU54F/cypress-circleci/tree/master)
[![npm version](https://badge.fury.io/js/cypress-circleci.svg)](https://badge.fury.io/js/cypress-circleci)

## A CircleCI Parallel Workflow Project Bootstrap

Features

- [X] Output a CircleCI v2.1 Workflow template for all spec files ending in `spec.js` located at `cypress/integration`
- [X] Reporting with `Mochawesome`
- [X] Report merging with custom script
- [X] Slack Report notifications with `cypress-slack-reporter`

## Instructions

1. run `npm install cypress-circleci --save`
2. run `node node_modules/.bin/cypress-circleci` to generate CircleCi config in `./circleci/parallel_config.yml`. (Rename to `config.yml` to use - avoids overwriting existing configs)
3. Add a env var `SLACK_WEBHOOK_URL` with your Slack webhook.
4. Run the workflow in CircleCI by pushing a commit with your renamed `config.yml` in `./circleci/config.yml` in your commit.


## To do
- [ ] Report merging with `Mochawesome-Merge`
- [ ] recursive folder search
- [ ] ts file support / bootstrapping
- [ ] user modifiable path to specs
- [ ] cli runner
- [ ] logger
- [ ] create orb

## Credits

See initial [Blog post](https://testdriven.io/blog/running-cypress-tests-in-parallel) by [testdrivenio/cypress-parallel](https://github.com/testdrivenio/cypress-parallel) for inspiration
