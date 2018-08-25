##### Here's the source of this exercise:

https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/development_environment

1. make app folder
2. cd into the app folder
3. npm init (while terminal is within the app folder)
4. chances are there is a package.json in your folder which looks like This

<pre>
{
  "name": "myapp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
</pre>

5. Install express in the directory (done in terminal)

<pre>
npm install express --save
</pre>

The auto-updated package looks like this now. Meaning, the dependencies have been updated.

<pre>
{
  "name": "comprehend-packagejson",
  "version": "1.0.0",
  "description": "\"The purpose of this simple npm init is to understand why npm creates package.json to manage dependencies\"",
  "main": "index.js",
  "scripts": {
    "test": "houseparty"
  },
  "author": "Ram N",
  "license": "MIT",
  "dependencies": {
    "express": "^4.16.3"
  }
}
</pre>

To use the library you call the require() function as shown below. (add these to a new file called index.js in the app folder)

<pre>
const express = require('express')
const app = express();

app.get('/', (req, res) => {
  res.send('Hello World!')
});

app.listen(8000, () => {
  console.log('Example app listening on port 8000!')
});
</pre>

You can start the server by calling node with the script in your command prompt:

<pre>
node index.js
Example app listening on port 8000
</pre>
