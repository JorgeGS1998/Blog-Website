##iniciar projeto##

command list 

1. npm init 
2. npm install node  
3. npm install express  
4. npm install body-parser 
5. npm install nodemon   

command line start application: npx nodemon app.js 

estrutura do app.js 

//jshint esversion:6

const express = require("express");
const bodyParser = require("body-parser");
const ejs = require("ejs");


const app = express();
const port = 3000; 

app.set('view engine', 'ejs');

app.use(bodyParser.urlencoded({extended: true}));
app.use(express.static("public"));


/*HOME PAGE*/
app.get("/", function(req, res){
  res.render("home");
})


app.listen(3000, function() {
  console.log(`Server started on http://localhost:${port}`);
});

