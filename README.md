# Monorepo Test

Just a very simple test how to work with monorepo.

**The problem:** one monorepo, multiple services and on each commit everything is "deployed", or better, each service is  checked with lint, then tested, built and deployed. This is a performance problem and would be better if service workflow can be ignored if nothing changed in that specific service.

## How to test the setup

Single service update:

1. update `service-1/index.js` file
1. commit and push the change
1. check if only *Service 1* workflow was triggered

Multiple service update in multiple commits:

1. update `service-1/index.js` file
1. commit the change
1. update `service-2/index.js` file
1. commit the change
1. push
1. check if *Service 1* and *Service 2* workflows were triggered
