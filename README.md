# Web-Scraping-Wallapop-using-Slenium
This is my code to web scrape the second hand items website "Wallapop" in Barcelona and obtain information on listings for used bicycles.

# WALLAPOP ASSIGNMENT - TEAM B10
### OBTAINGING SECOND BIKES IN THE BARCELONA AREA THAT FULFILL CERTAIN CRITERIA

The code below will walk you through the web scraping process to follow in order to obtain data about second hand bikes listed on the Wallapop website in Spain - Barcelona and create a ```DataFrame``` that appends all the listings and another ```DataFrame``` that will give us a summary of the data obtained (based on bike type, condition, and average listing price).

We would like to look for bike types that fall under three chriteria: ```Bicicletas de carretera```, ```MTB```, and ```Plegables```.

Next, for each bike type of the three mentioned, we would like to limit the search for 3 bike states/conditions: ```"Nuevo"```, ```"Como Nuevo"```, and ```"En Buen Estado"```.

Therefore, to do the above, the below code follows the below architecture:
1. We import the necessary libraries, initiate a driver instance, and load the ```Wallapop website```
2. We apply the necessary preliminary filters to suit our item search, location, and price restrictions
3. We select the first bike type, and then the first bike condition, and scrape the listings for the needed data (a for-loop will help us deal with the search and will make our code easier to read and understand). Our search will be limited to 250 listings in case more exist.
4. Step 3 is repeated untill we have obtained all the data about every bike type and bike condition
5. The data is then aggregated in a ```DataFrame``` ```df```
6. A summary ```DataFrame``` ```agg```  is created to group as a summary of the data obtained (based on bike type, condition, and average listing price)


With that said, let's get to work! First, let's begin by importing the required libraries.
