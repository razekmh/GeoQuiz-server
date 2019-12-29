# ucesmmh_server

## System Requirements:
The server uses the resources available to the class and was edited on a windows machine connected to the ubuntu server which we were provided access to during the class, to run the applications and the server these resources are needed
### Software Requirements:
- A vertuial or physcial machine to host the server
- Node.js installation
- A recent browser (the apps were tested on chrome and firefox most reacent versions)
### Hardware Requirements: 
- An android phone running android version 4.4 and up for the phonegap application

## Deploying the code:
- Download all the three repositories to your machine
- Start a command line and go to the directory which you downloaded the server repository
- Start the server, either in debug mode by typeing `node httpServer.js` or run the server normally by typing `pm2 start httpServer.js`
- You should recieve a feedback message announcing the start of the server. 
- If you have started the server in debug mode then start a new command line, if not then you can carry on using the same which you are using. 
- Go to the directory where you downloaded either the `ucesmmh_questions` or `ucesmmh_quiz` depending on which application you wish to start first.
- Go to the `ucesmmh` folder
- Start the phone gap application by typing `phonegap serve`
- You should recive a feedback message announcing the start of the server.
- Open a browser window and type the web address which the server is hosted at ( in case of running the application from within UCL network and on the server provided in the class that should be http://developer.cege.ucl.ac.uk: followed by your port id) 
## Testing the code:
To test the code you should start the server in the debug mood, then run phone gap application as well, and moniter the feedback messages displayed in both command prompts. Additionally some `console.log()` functions maybe added to the code to check the internal route of data. 
## Files in the repository:
The repositry contains only one file which is `httpServer.js` it contains several functions. The table below explains the main functions 

Function Name | Function Role 
--------------|--------------
app.use | Adding functionality to allow cross-domain queries when PhoneGap is running a server
app.post '/reflectData'| Reflects back the sent data to the front end
app.post '/uploadQuestion' | Uploads the questions submited to the database 
app.post '/uploadAnswer' | Upload the answers submited to the database
app.get '/getQuizPoints/ | Download the question points of a specific user from the database and send them to the front end to be added to the map
app.get '/getAllQuizPoints' | Download the question points of all users from the database and send them to the front end to be added to the map
app.get '/getClosestFive' | Download the question points of the closest five questions to the user location from the database and send them to the front end to be added to the map
app.get '/getRanking/ | Gets the ranking of a specific user and submit it to the front end to be displayed in the web page
app.get '/noCorrect/ | Gets the number of the correctly answered questions from the database and sends it to the front end to be posted on the webpage
app.get '/getLastFive/ | Gets the last five answered questions by the user from the database and send them to the front end to be displayed on the map
app.get '/getInccorectQuizPoints | Gets the question points which were not answered correctly by the user and send them to the front end to be displayed on the map 
app.get '/getlastWeek' | Gets the questions which were added last week 
app.get '/getMostDifficult' | Gets the most difficult questions from the database and send them to the front end to be displayed in a table
app.get '/getTopFive' | Gets the top five scores of users from the database and send them to the front end to be displayed in a graph 
app.get '/getPastWeekRate | Gets the participation rates of the all the users or a spesific user based on the input parameters, and then send the data to the front end to displayed in a graph 





## Third Party code:

All the applications mentioned above were based on examples provided in the Web and Mobile Module 
