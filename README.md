#swagger-github

![screenshot](screenshot.png)

outputs a swagger 2.0 document referencing swagger documents found via github api search.


installation
------------

```
npm install -g swagger-github
```

usage
-----

rate limited api requests
* authenticated: 30 requests per minute.
* unauthenticated: 10 requests per minute.

```
#unauthenticated
swagger-github

#authenticated
GITHUB_TOKEN=<your-generated-token> swagger-github

#specified repos query (default is "user:rapid7")
REPO_QUERY="stars:>10000" swagger-github

#specified swagger query (default is  "swagger in:path extension:json" )
SWAGGER_QUERY="swagger.json in:path" swagger-github

#authenticated repo query with default swagger query
GITHUB_TOKEN=1234566789 REPO_QUERY="stars:>5000" swagger-github
```
