# vocabserver-deploy

# how to deploy vocabserver

- cp .dotenv .env
- edit .env to the build tag you want to deploy (default latest if not specified)
- run docker-compose up

# dotenv variables

- BUILD_TAG: the build tag you want to deploy(default latest if not specified)
- HOST_PORT_IDENTIFIER_SERVICE: the port identifier you want to deploy(default 3033 if not specified)
- CONTAINER_PORT_IDENTIFIER_SERVICE: the port identifier you want to deploy(default 80 if not specified)
- HOST_PORT_DATABASE_SERVICE: the port identifier you want to deploy the triplestore database to (default 8890 if not specified).

The HOST_PORT_DATABASE_SERVICE variable is used in the following service variables:

- database.environment.MU_SPARQL_ENDPOINT
- vocab-fetch.environment.MU_VIRTUOSO_ENDPOINT
- content-unification.environment.MU_SPARQL_ENDPOINT
- content-unification.environment.MU_SPARQL_UPDATEPOINT
- content-unification.environment.MU_AUTH_ENDPOINT
- vocab-configs.environment.MU_SPARQL_ENDPOINT
- vocab-configs.environment.MU_SPARQL_DIRECT_UPDATEPOINT
- vocab-configs.environment.MU_AUTH_ENDPOINT
