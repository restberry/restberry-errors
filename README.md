Restberry-Errors
================

## Install

```
npm install restberry-errors
```

## Response examples

* **401** UNAUTHORIZED
```
2014-05-11T13:26:27.758Z|172.16.122.129|GET|</api/v1/foos/536f7a835bc82212a9e78624> <{}>
2014-05-11T13:26:27.758Z|172.16.122.129|401|<{
  "error": {
    "statusCode": 401,
    "property": "",
    "title": "Unauthorized",
    "message": "Need to be logged in to perform this action.",
    "devMessage": "Requested <GET> </api/v1/foos/536f7a835bc82212a9e78624> with data <{}>. Make sure you are logged in and authenticated. {}"
  }
}>
```

* **403** FORBIDDEN
```
2014-05-11T13:26:27.758Z|172.16.122.129|GET|</api/v1/foos/536f7a835bc82212a9e78624> <{}>
2014-05-11T13:26:27.758Z|172.16.122.129|403|<{
  "error": {
    "statusCode": 403,
    "property": "",
    "title": "Forbidden",
    "message": "You are not authorized!",
    "devMessage": "Requested <GET> </api/v1/foos/536f7a835bc82212a9e78624> with data <{}>. Make sure you're logged in with the correct credentials."
  }
}>
```

* **409** CONFLICT
```
2014-05-11T11:55:55.368Z|172.16.122.129|POST|</api/v1/foos> <{
  "name": "test"
}>
2014-05-11T11:55:55.358Z|172.16.122.129|409|<{
  "error": {
    "statusCode": 409,
    "property": "foo",
    "title": "Conflict",
    "message": "There already exists a 'foo' object with these properties.",
    "devMessage": "Requested <POST> </api/v1/foos> with data <{\"name\":\"test\"}>.'
  }
}>
```

* **500** SERVER ISSUE
```
2014-05-11T13:23:37.820Z|172.16.122.129|POST|</api/v1/foos> <{
  "name": "test"
}>
2014-05-11T13:23:37.821Z|172.16.122.129|500|<{
  "error": {
    "statusCode": 500,
    "property": "",
    "title": "Server Issue",
    "message": "We're on it!",
    "devMessage": "Requested <POST> </api/v1/bars> with data <{\"name\":\"test\"}>."
  }
}>
```