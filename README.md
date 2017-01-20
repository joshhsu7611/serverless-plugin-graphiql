# serverless-plugin-graphiql

> Runs a local http server for graphiql and your graphql handler

[![Build Status](https://travis-ci.org/bencooling/serverless-plugin-graphiql.svg?branch=master)](https://travis-ci.org/bencooling/serverless-plugin-graphiql)
[![Coverage Status](https://coveralls.io/repos/github/bencooling/serverless-plugin-graphiql/badge.svg?branch=master)](https://coveralls.io/github/bencooling/serverless-plugin-graphiql?branch=master) [![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)
[![Npm Version](
https://img.shields.io/npm/v/serverless-plugin-graphiql.svg)](https://www.npmjs.com/package/serverless-plugin-graphiql)


## usage
See `/example` directory to see how easily it's done!  

**Steps**  
1. Create a lambda function named graphql that implements a graphql server
2. Add `graphiql` to serverless plugins array
3. Run `sls graphiql` command from root of serverless project
4. Visit `localhost:8000/graphql` to view graphiql in browser


## about

- This plugin creates two endpoints:  
```
GET /graphql
POST /graphql
```
- Once graphiql is running, you can also make requests via cli:
```bash
curl -X POST \
-H "Content-Type: application/json" \
-d '{"query": "{ hello }"}' \
localhost:8000/graphql
```
