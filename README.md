# fetchapi
Exercises using FETCH , API 

A simple API using fetch.

1 ----
Instructions: Post Form


create a page index.html containing a form with:
an input for a title
a textarea for an article
a button to submit the form
add a script element wich will:
listen for click event on the button
stop the event propagation (the page must not reload when you click on the button)
send a POST request to new-article.php with the form content
create a page new-article.php wich:
check for the presence of title and content in the $_POST variable and return the appropriate HTTP code if the parameters are missing

2 ----
Instructions: Post JSON

An API is available at http://192.168.1.152:8080/, you can get the code at https://github.com/aitva/blog-api. You will need to update index.html to:

extract the data from your form into a JS object
transform the object into a JSON string
use fetch to send the JSON string to the following URL: http://192.168.1.152:8080/article/:
the server expects an URL parameter: id={name}
the server expects a valid Content-Type
the server will answer using HTTP status

3 ----
Instructions: Get JSON

Once we have sent our data to the API we are able to retrive them at http://192.168.1.152:8080/articles/ and update our page to display the articles. You will need to update index.html to:

add a section element to display the article
add a display function in a script to:
retrieve data from the server using fetch
transform the data into a JS object
loop over the object and create an article containing a title and a p
call display when you start the script
call display when the user post a new article
