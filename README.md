# Templates

## Server starting code Flask
```
from flask import Flask

app = Flask(__name__)


@app.route("/")
def hello_world():
    return "<p>Hello World!</p>"


if __name__ == "__main__":
    app.run(debug=True)

```

## Server starting code Javascript
```
const express = require("express");
const bodyParser = require("body-parser");
const ejs = require("ejs");

const app = express();

app.set('view engine', 'ejs');

app.use(bodyParser.urlencoded({extended: true}));
app.use(express.static("public"));

app.get("/", (req, res) => {
    res.send("<h1>Hello World!</h1>")
});

app.listen(3000, function () {
  console.log("Server started on port 3000");
});
```
