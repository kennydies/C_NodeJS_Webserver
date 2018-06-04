###Use the Express Module
>const express = require('express');  
var app= express();  
>
>app.get('myURL', (req, res) => {  
&&res.send(myObject);  
})

###Express Middleware
Middleware functions are functions that have access to the request object (req),   
the response object (res), and the next middleware function in the application’s   
request-response cycle. The next middleware function is commonly denoted by a  
variable named next.

Middleware functions can perform the following tasks:
* Execute any code.
* Make changes to the request and the response objects.
* End the request-response cycle.
* Call the next middleware function in the stack.

>app.use((req, res, next)=>{  
&&next();  
});

**Middleware is executed by appearing Order.**

###Handlebars
Handlebars provides the power necessary to build semantic templates effectively.

Load the module:
>const hbs = require('hbs');

Register partials:
>hbs.registerPartials(__dirname + '/views/partials');

Register helper:
>hbs.registerHelper('myCommandName', () => {  
    &&return myStuff;   
});

Render a Page:
>app.get('myURL', (req, res) => {  
    &&res.render('myPage.hbs', {  
        &&&&//set variables for hbs  
        &&&&pageTitle: 'About Page'  
    &&});  
});

Variables injections
>{{myVar}}

Partials injections:
>{{> header}}

###

###