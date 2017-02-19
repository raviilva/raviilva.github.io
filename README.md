## Website Performance Optimization portfolio project


This is the final product of Udacity's web optimization project. In this document, I will explain how to run the project, and then explain what I did to fix the optimization issues.

How to Run
-----------

simply click on this URL: https://github.com/raviilva/raviilva.github.io



How to check the Page Speed - index.html
----------------------------

In order to check the page speed of index.html,go to https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fraviilva.github.io.%2F&tab=mobile and run https://raviilva.github.io./

My Optimization Process
-------------------------

I minified the pizzeria.jpg and progfilepic.jpg and added the font information direclty in the file in order for it to run more efficiently. In order to increase the page speed further I added the link to the css/print.css file. 

In order to prevent render-blocking Javascript for pizza.html, I restructured the code in main.js to prevent jank in the moving pizzas. I also eliminated the repeating code so that the pizza slider would function faster. 

I amended document.querySelectorAll to document.getElementsByClassName() in order for Web API call to run faster. Creadted a local variable to save document.getElementsByClassName('randomPizzaContainer') outside the loop, so the DOM is not explicitly touched in every iteration. And reduced the number of background pizzas to 24.

Finally I included the transform: translateZ(0); in order to increase the sites performance.