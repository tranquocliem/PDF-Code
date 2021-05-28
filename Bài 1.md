# **<div style="text-align:center;">Bài 1. Kết Nối Nodejs Với MongoDB :tada:**

<br/>

## **1. File package.json** :banana:

<br/>

> ### **npm i express mongoose nodemon**

<br/>

```json
{
  "name": "training",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.17.1",
    "mongoose": "^5.9.28",
    "nodemon": "^2.0.4",
  }
}
```

<br/>

<div style="page-break-after: always;"></div>

## **2. File Server.js** :banana::banana:

<br/>

```js
const express = require("express");
const mongoose = require("mongoose");
const app = express();

const db = require("./config/key").mongoURI;

mongoose
  .connect(db, { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => console.log("MongoDB Connected...."))
  .catch((err) => console.log(err));

const PORT = process.env.PORT || 8080;
app.listen(PORT, console.log(`Server Run With Port ${PORT}`));

```

---
<br/>
<br/>
<br/>

<div style="font-size:55px;text-align:center;font-family:Brush Script MT">The End

<br/>
<br/>

## <div style="font-size:55px;text-align:center;">:wave::wave::wave::wave::wave:</div>
