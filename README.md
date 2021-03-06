# Week 10

## Mongoose

### Question #1

Describe the differences between a SQL and NoSQL DB, and when you might use each.

```text
Your answer...
SQL is a relational db comparing data through Foreign Keys and schemas, while NoSQL uses collections to insert data similar to JSON entries, not schemas.
```

### Question #2

What's wrong with this mongoose code and how might we fix it?
(Hint: Assuming there is a document with a name of "Bob", why is results not an author model on the second line?)

```js
var results = AuthorModel.find({name: "Bob"});
console.log(results);
```

```js
var results = AuthorModel.find({name: "Bob"}, function(results){
  console.log(results);
});
```

### Question #3

Convert the following ActiveRecord sequence to Mongoose:

```rb
Instructor.findOne({name: "Andy"), function(err, andy){
  andy.wishlist_items.push({description: "Resin Laying Deer Figurine, Gold");
  andy.save();
});
```

```js
// Your answer...
```

### Question #4

Convert the following create method in Mongoose to ActiveRecord.

```js
  var authors = {
  create: function(req, res){
  var author = new AuthorModel({name: req.body.name})
  author.save(function(err){
    if (!err){
      res.redirect("authors")
    }
  })
  }  
}
```

```rb

```
## Express

### Question #5

How does module.exports help us with separation of concerns?

```text
it keeps related functions in separate files
```

### Question #6

Write one Express route for each of the four HTTP methods.

Then, make each route respond with a one-word string containing the RESTful action that would most likely be associated with this route.

```js
var express = require("express");
var app = express();

// Your code starts here...

```

```js
app.get("/", function(req, res){
  response.send("index");
});
app.post("/", function(req, res){
  response.send("create");
});
app.put("/:id", function(req, res){
  response.send("update");
});
app.delete("/:id", function(req, res){
  response.send("delete");
});
```
### Question #7

Describe the differences between Express and Rails as backend frameworks.

```text
Rails is very formal and Express is more informal and flexible as far as where you can put certain files.
```

### Question #8

What is the importance of using body-parser in our express application for post requests?

```js
Body-parser is processed through middleware function when a post request is made.
```
