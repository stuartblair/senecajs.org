---
layout: splash.html
---

#### A bare bones microservice
```javascript
var seneca = require('seneca')()

seneca.add({ role:'user', cmd:'login' }, function (args, callback) {
  callback(null, { loggedIn:true })
})

seneca.listen()
```

#### A bare bones client
```javascript
var seneca = require('seneca')()
var client = seneca.client()

client.act({ role:'user', cmd:'login' }, function (err, result) {
  console.log(result.loggedIn)
})
```
