---
title: Tutorials Notes
description: A guide in my new Starlight docs site.
---

**Video 1**
```js

import http from 'node:http';

// Node.js requestListener() Function
// The requestListener function is the function that is executed each time the server gets a request:

// The first parameter, the Request object, represents an IncomingMessage object.
const server = http.createServer((request, response) => {
    console.log(request.headers);
    response.write('hello world', function () {
        console.log('data is written');
    })
    respnse.end(request.url);
});

server.listen(8000)


```


```js


import http from 'node:http';
const server = http.createServer((request) => {
    console.log(request);
});
server.listen(8000);

```



```js
import http from 'node:http';

http.createServer((request, response) => {
    // Access properties of the IncomingMessage object
    console.log(request.method); // Get the HTTP method of the request
    console.log(request.url); // Get the URL of the request

    // Read data from the IncomingMessage object
    // we can only read data from rquest object if we have sent data in request.. to send data in request use 'insomnia' or postman then you will be able to see the received bytes in console
    request.on('data', (chunk) => {
        console.log(`Received ${chunk.length} bytes of data.`);
    });

    request.on('end', () => {
        console.log('Request ended.');
        // Send response back to the client
        // ServerResponse object handles response
        response.end('Hello, world!');
    });
}).listen(8080);

```

---

**Video 2**

event loop architecture

listening/registering an event
un registering an even
`process.exit()`

---

**video 3**

request.url, request.method, request.headers

---

**video 4**


```js
res.setHeader('Content-Type', 'text/html');
res.write('<html>');
res.write('</html>');
res.end();
```
---

**Extras**



**Video 5**

**Video 6**
node event loop

**Video 7**
"start": app.js
npm start
npm run start-server
`npm install nodemon --save-dev`
nodemon start
**Video 8**
debugging

debugging configurations

```json
{
    "type": "node",
    "request": "launch",
    "name": "Launch Program",
    "program": "${workspaceFolder}/app.js",
    "restart": true,
    "runtimeExecutable": "nodemon",
    "console": "integratedTerminal"
}
```

Above configurations look for nodemon globbaly so install 
nodemon globbaly.
`npm install nodemon -g`


**Prisma video**
Traversy Media
https://www.youtube.com/watch?v=CYH04BJzamo&ab_channel=TraversyMedia
