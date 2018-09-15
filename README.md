# hello-api
SpringBoot, Swagger, Docker and Postgres for a little (LOL) hello world api service


## What's this?

A minimal app that I like to use for a starting microservice projects.  You can find similar things out there so YMMV but I like this combo of tech. 

* SpringBoot - Not as simple as dropwizard or other micro frameworks, but comes with EVERYTHING via starters so when your microservice isn't so micro you have patterns to follow rather than roll your own
* Swagger - Defines the api contract and is used to generate interfaces that your controllers implement
* MyBatis Starter and Flyway - Plain ol sql thank you very much and flyway is there out of the box too.
* Docker - Image that can be deployed anywhere is the artifact produced, so that's nice
* Postgres - Alpine Docker image makes this a painless real db


## How to use

* Launch postgres in a docker container https://hub.docker.com/_/postgres/
* Edit your `application.properties` with the access params
* Edit the swagger doc at `src/main/resources/v2/api-doc/swagger.yaml`
* Generate the interfaces with `mvn compile`
* Hack your controllers to impl the interface
* Build your docker image `mvn package`
* Launch your docker image `docker run ... `
