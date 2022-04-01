# Basic-REST-API
A basic REST API  -- uses GET, POST, PUT, and DELETE.
To run (Visual studio code).... you will need
-VS Code, nodejs, expressjs, and sqlite3
-A few commands to run!
Intsalling node:
in the terminal ---> type in npm install -g npm
Installing express: npm install express --save

SQLITE:
npm install sqlite3
Then, in the terminal, type in
sqlite3 mydatabase.db
then... .read init_db.sql

Now the database is connected to the application, and you're ready to go!
To make requests easier, you can go to hopescotch.io.

In the terminal, type in node index.js....
then begin making requests once the program says REST API listening on port 3000, database is connected!
All routes begin with localhost:3000/api/

-------------------------------------------------------------------------------------------------------
NAME: ALEXANDER RABETTE
COURSE: CSC342
INSTRUCTOR: DR. DYLAN SCHWESINGER
ASIGNMENT: MIDTERM PROJECT

-------------------------------------------------------------------------------------------------------

DOCUMENTATION FOR APP.GET

-------------------------------------------------------------------------------------------------------
DATABASE.
There are two tables with related data stored into the DB.
One table is named Players, containing career statistics about both former and current NFL players.

The other table is named Coaches, containing career statistics about both former and current NFL Coaches.

--------------------------------------------------------------------------------------------------------

APP.GET HAS 4 TOTAL ROUTES

--------------------------------------------------------------------------------------------------------
When going to '/api/players'
A list containing all of the current players in the database will be returned

When going to '/api/coaches
A list containing all of the current coaches in the database will be returned

When going to '/api/players/:id'
Type in the ID of the player you would like to view. If it does not exist, the status code will be 404 not found.
If successful, the status code will be 200OK, and the player with the corresponding ID passed into the URI will be returned.

When going to '/api/coaches/:id'
Type in the ID of the coach you would like to view. If it does not exist, the status code will be 404 not found.
If successful, the status code will be 200OK, and the coach with the corresponding ID passed into the URI will be returned.

--------------------------------------------------------------------------------------------------------------------------

APP.POST HAS 2 ROUTES

When doing POST '/api/players'
You MUST format the entire body as follows:


     "Name": "name here",
    "Age": age here,
    "Position": "Position here, abbreviated",
    "Team": "Team name here, do not include the city",
    "JerseyNumber": Jersey number here. Whole numbers only,
    "PPG":  Average number of Points per game here,
    "CareerTD": Total career touchdowns here,
    "YearsPlayed": Total number of years played here

When doing POST '/api/coaches'
You MUST format the entire body as follows:


    "Name": "Name goes here",
    "Age": age here,
    "Team": Team name here, do not include the city,
    "YearsCoached": Number of years coached here,
    "Wins": Total career wins as a coach here,
    "Losses": Total career losses as a coach here,
    "WLPERCENTAGE":  Win-loss percentage here  ex. 0.609,
    "SBWON": Total number of super bowl wins here,
    "CONFRENCETITLES": Total number of confrence title wins here
    -----------------------------------------------------------
    
    WHEN DOING  PUT: '/api/players/:id
    
    INCLUDE THE ID OF THE PLAYER YOU WANT TO UPDATE
    
    Format the body as follows:
     "Name": "name here",
    "Age": age here,
    "Position": "Position here, abbreviated",
    "Team": "Team name here, do not include the city",
    "JerseyNumber": Jersey number here. Whole numbers only,
    "PPG":  Average number of Points per game here,
    "CareerTD": Total career touchdowns here,
    "YearsPlayed": Total number of years played here

Update the attributes desired, and submitting will update. Confirm with GET

WHEN DOING PUT: '/api/coaches/:id

INCLUDE THE ID OF THE PLAYER YOU WANT TO UPDATE

Format the body as follows:
    "Name": "Name goes here",
    "Age": age here,
    "Team": Team name here, do not include the city,
    "YearsCoached": Number of years coached here,
    "Wins": Total career wins as a coach here,
    "Losses": Total career losses as a coach here,
    "WLPERCENTAGE":  Win-loss percentage here  ex. 0.609,
    "SBWON": Total number of super bowl wins here,
    "CONFRENCETITLES": Total number of confrence title wins here

Update the attributes desired, and submitting will update. Confirm with GET

-----------------------------------------------------------------------------------------------------------------------
WHEN DOING DELETE '/api/players:id' AND '/api/coaches:id .....
You MUST include the ID of the resource you want to delete from the DB. Doing so will return a 204 no content response. Upon trying to
GET of the resource you just deleted, you will find that you will get a 404 not found confirming that the item is deleted.


