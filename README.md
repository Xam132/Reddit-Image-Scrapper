# Reddit-Image-Scrapper

Using Beautiful Soup, Selenium to scrape subreddits to obtain img files form top of the month

Sometimes multiple page images arent downloaded and ads are also downloads, so these bugs needs to be fixed


# How it works 

Reddit has infinite scroll, so we cant just use requests to get a lot of images.
Thus here we utlise selenium. Selenium allows us to scroll through the webpage ad thus updates the page source to include the new images obtained by scrolling too.
This is done by continuously looping and updating the current screen height. Here we wait for a second for the page to load the next part.
To check if we have reached the bottom of scroll we check if the screen height has changed over some time ( 20 - 30 sec ). If it remains same then we exit the loop then use Beautiful Soup to obtain the images
Here we seperate the posted images using Beautiful Soup and get its content. We then write this content in a new img file and save it in Reddit/img/{{subreddit_name}} folder.


# Modules used 

Selenium, requests, Beautiful Soup, os, time
