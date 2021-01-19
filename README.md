# MAM---Documentation

**Deployed site:**
https://mammogrammo.netlify.app/

**Official Repo:**
https://github.com/MAM-MERN

**Tom's Working Fork:**
https://github.com/dunerztd/MAM-Server

**Alisa's Working Fork:**
https://github.com/alisay/MAM-Client

---
## Planning

We decided to split the application development into Backend and Frontend with Tom and Alisa handling them respectively. Alisa is stronger in react than Tom and since Tom handled the ADD and DFD and Alisa designed the wireframes in Part A, this pathway made the most sense.

Sprints will be weekly in duration with a standup on Mondays deciding the tasks to completed for the week. We will recovene at the end of the week to update each other on our progress. Informal communication will be ongoing throughout the week.

All tasks will be added to Trello as tickets with labels indicating person to complete the task, whether it's server or client and a difficulty rating. The ratings are 1-Easy, 2-Medium, 3-Hard, 5-Very Hard, 8-Needs Breaking Down, 11-Needs Break Down.

There are 5 weekly sprint between Part A submission and Part B submission. We anticipate they will be broken down this way:<br>
Week starting 14 December: Planning<br>
Week starting 21 December: First prototype<br>
Week starting 28 December: Aim for usable final product<br>
Week starting 4 January: User testing<br>
Week starting 11 January: Finalize documentation ready for submission

---
## Libraries/Dependencies

### Server

**Library/Dependency**|**Description**
:-----|:-----
**aws-sdk** | Amazon web services software development kit for javascript. Allows developers to connect to AWS services through javascript objects
**connect-mongo** | Session store for MongoDB
**cors** | Enables CORS in an Express app
**dotenv** | Loads environment variables into process.env
**ejs** | Generates HTML markup with embedded javascript
**express** | Web application framework for Node
**express-fileupload** | Express middleware for uploading files
**express-session** | Session middleware for Express
**mongoose** | Object Data Modeling library for MongoDB and Node
**mongoose-bcrypt** | A mongoose plugin for encrypting fields with bcrypt
**passport** | Authentication middleware for Express/Node
**passport-local** | Passport strategy for authenticating with a username and password
**chai** | An assertion library for Node
**mocha** | Javascript testing framework
**nodemon** | Automatically restarts a Node application when changes are made

### Client

|**Library/Dependency**|**Description**
:-----|:-----
|**@material-ui/core** | A React UI framework comprising components, styles, themes and icons
**@material-ui/icons** | Material-UI icons as React components
**@material-ui/lab** | Material-UI components not available in core
**@react-google-maps/api** | React components wrapping the Google maps Javascript API
**@testing-library/jest-dom** | Custom Jest matchers for testing the DOM
**@testing-library/react** | React component testing
**@testing-library/user-event** | Simulates user interaction with the browser for testing purposes
**axios** | Promise based HTTP client for the browser and Node
**fontsource-roboto** | Self-host the 'Roboto' font
**google-maps-react** | A Google Map React component library
**react** | A Javascript library for building user interfaces
**react-dom** | Renders React components in the DOM
**react-geocode** | Transforms a location into it's longitude and latitude coordinates
**react-router-dom** | DOM bindings for React Router
**react-scripts** | Create React App scripts and configuration
**web-vitals** | Library for measuring all the Web Vitals metrics

---
## Sprints

<details>
  <summary>14/12/20 - 20/12/20</summary>
  <img src="./docs/trello_screenshots/Screen_Shot-1.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-2.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-3.jpg">
</details>

<details>
  <summary>21/12/20 - 27/12/20</summary>
  <img src="./docs/trello_screenshots/Screen_Shot-4.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-5.jpg">
</details>

<details>
  <summary>28/12/20 - 3/1/21</summary>
  <img src="./docs/trello_screenshots/Screen_Shot-6.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-7.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-8.jpg">
</details>

<details>
  <summary>4/1/21 - 10/1/21</summary>
  <img src="./docs/trello_screenshots/Screen_Shot-9.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-10.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-11.jpg">
  <img src="./docs/trello_screenshots/Screen_Shot-12.jpg">
</details>

<details>
  <summary>11/1/21 - 19/1/21</summary>

</details>

---
## Manual Testing

**Test**|**Expected Outcome**|**Actual Outcome**
:-----:|:-----:|:-----:
I want to be able to log in, to ensure security is not breached |
I want to be able to add new artworks, as they are commissioned or acquired by the City collection, to ensure information is up-to-date |
I want to be able to edit artworks I have added, so that I may correct any data entry errors I may have made |
I want to be able to delete artworks I have added, so that I may correct any data entry errors I may have made. |
I want to be able to log out, to ensure that no-one else using my computer can inadvertently add, delete or edit artworks |
Deny access if username/password is incorrect |
break | break
I want to be able to view all artworks on a map, so I can see their distribution in the City |
I want to view all artworks in a complete list, so I can browse all artworks |
I want to view details of individual artworks, so that I can learn the name of the artist, the name of the artwork, when it was made and installed, and any other interesting information |
I want to see a photo of the artwork, so I can decide whether it is worth visiting |
I want to know how long it will take me to navigate to the artwork |
I want to be able to search for an artwork, based on a keyword, so that I can refine the list of artworks I wish to see |
I want to know who made the application I am using, and why, so I can be assured of its integrity and use value |
I want to be able to contact the makers of the app, so that I can congratulate them on their fine work |
break | break
Map correctly shows current location |
App restricts access to add/edit/delete routes if user is unauthenticated |
Image loads when pin is clicked |
Shows errors when admin forms aren't filled in correctly | 

## User Testing - Development/Production

<video controls>
<source src="./docs/videos/map-search.webm type="video/webm">
</video>

---
## Part A - Documentation
<details>
  <summary>Click to Expand</summary>

  # T3A2-A - MERN Application (Part A)
A group project between Alisa Blakeney and Tom Dunstan

## R1. Description of your website, including:
- Purpose
- Functionality / features
- Target audience
- Tech stack	

This application displays the location of public artworks in City of Melbourne. It can be used to navigate between artworks and learn more about each. It has three main views: 
1. a landing page with a scan-and-scrollable map that shows the user's location and pin markers at the location of each artwork.
2. an about page with information about the public art collection, and with a colophon. 
3. a search view with an open text field that searches the title and artist of the artwork [with the option to view all as an alphabetically sorted list]

From the map view or the search results view, you can navigate to see a page with a photograph of the artwork and the metadata including title, artist, location, date, materials. 

Registered administrators can log in to add additional artworks to the database, and edit or delete artworks they have added. 

### Additional Features
- wayfinding (find the best route from you to another artwork, from one artwork to another)
- regular users can login to create a "favourites list" of artworks
- a "share" button that generates a shareable link

### Target Audiences
- Local residents interested in finding out more information about the artworks in their home town.
- Tourists interested in learning about the culture of the town they are visiting.
- Those with an academic interest in art, wanting a basic entry point into researching individual public artworks

### Tech stack

Frontend:
- React
- Axios
- Turf JS
- Netlify

Backend:
- Node
- Express
- Mongoose
- MongoDB
- Express Session
- Passport
- AWS S3
- Heroku
- Atlas

Testing:
- Jest

Source Control:
- Git
- GitHub

Documention and Planning:
- Trello
- Figma
- Lucid Chart
- Diagrams.net

---
## R2. Dataflow Diagram	

<details><summary>Click to expand</summary>

![Dataflow Diagram](./docs/Part-A/Diagrams/DDF.jpeg)
</details>

---	
## R3. Application Architecture Diagram

<details><summary>Click to expand</summary>

![Architectural Diagram](./docs/Part-A/Diagrams/AAD.png)
</details>

---	
## R4. User Stories	

#### Personae 
<details><summary>Click to expand</summary>

##### Felicity

Felicity is the curator of public art for City of Melbourne. She has a Master of Arts in curatorial practice for the public space. She is 35 years old, identifies as a woman, and is married with a small child. Since giving birth, she has become increasingly forgetful. She wants everyone to feel the same transformative power of art that she feels. She cares deeply about the people who live in City of Melbourne and wants to do her job as best as possible to represent them, the artists she works with, and feel professional integrity when she goes to sleep at night. 

##### Zal

Zal is a backpacker from Nijmegen. They have an international baccalaureate, but chose to travel before deciding on whether to attend tertiary education. They are 22 years old. Their first language is Dutch and but they speak a little English. They love bouldering, meeting new people, and adventure. 

##### Tim

Tim is a musician who lives in North Melbourne. He has studied various university degrees but never to completion. He is 67 years old. He has autism spectrum disorder, has a strong interest in local history, music, and tends to get overloaded by sensory information. Sometimes he works as a busker in public spaces of Melbourne. 

##### Mohammad

Mohammad is an artist who lives in Stoke on Trent. He is educated to PhD level in sculptural practice. He is 42 years old. He likes to travel, and his work at various large art institutions around the world means he has visited over one hundred countries. His art is exceptional, by virtue of his exacting standards.

</details>


#### User Stories
<details><summary>Click to expand</summary>

##### Users who are administrators

* As an administrator:
    * I want to be able to log in, to ensure security is not breached.
    * I want to be able to add new artworks, as they are commissioned or acquired by the City collection, to ensure information is up-to-date. 
    * I want to be able to edit or delete artworks I have added, so that I may correct any data entry errors I may have made.
    * I want to be able to log out, to ensure that no-one else using my computer can inadvertently add, delete or edit artworks.
    * I want to be able to reset my password, in the case that I forget or want it changed.
    * I do not wish to be able to edit artworks already in the database, as they are permanent installations and I do not wish to inadvertently delete their information.  

##### Users who are members of the general public

* As a member of the public:
    * I want to be able to view all artworks on a map, so I can see their distribution in the City. 
    * I want to view all artworks in a complete list, so I can browse all artworks.
    * I want to view details of individual artworks, so that I can learn the name of the artist, the name of the artwork, when it was made and installed, and any other interesting information. 
    * I want to see a photo of the artwork, so I can decide whether it is worth visiting. 
    * I want to know how long it will take me to navigate to the artwork. 
    * I want to be able to search for an artwork, based on a keyword, so that I can refine the list of artworks I wish to see. 
    * I want to know who made the application I am using, and why, so I can be assured of its integrity and use value. 
    * I want to be able to contact the makers of the app, so that I can congratulate them on their fine work. 

##### Felicity
* As a local goverment arts worker:
    * I want to have an easily accessible content management system, so as to be able to update the data on public artworks.
    * I want to be sure that my data is always consistent and correct, so that I can ensure I can providing accurate information to serve the residents in my constituency.
    * I want to have a way to reset my password when I forget what I set it to. 
    * I want the activities of my department represented in a way that is professional, clean and attractive, so I can feel a sense of pride about my work.

##### Zal
* As an urban explorer:
    * I want to easily see where sculptures and art installations are in the city I am visiting, so that I can plan out an itinerary for my bouldering activities. 
    * I want to learn more about the artworks I see as I am walking around, so that I can be educated on cultures other than my own. 
    * I want to make a note of my favourite artworks, so I can easily return to them on another day.
    * As someone with limited English, I want there to be clear informational graphics that guide my use of the app, so that I can navigate the different sections with ease. 

##### Tim
* As a troubadour and proud Melbournian: 
    * I want to know more about my city and the artworks I see daily, so that I can feel a warm sense of familiarity with my surroundings.
    * I want to be able to tell my audiences interesting facts about the monuments in front of which I busk, to add interest to my show.
    * I want to be routed directly to nearby artworks, so that I don't waste time in getting to work in the afternoons.
    * I want to see new artworks as they are added, so that I can be aware of where my council rates and taxes are being spent. 
    * I want the graphics and distracting information to be kept to a minimum, so as not to cause sensory overload. 

##### Mohammad
* As an artist whose artwork is in the City of Melbourne public art collection:
    * I want to be able to view my own artwork, even when I am not physically in Melbourne, so that I can experience some of the joy I am bringing to the local populace. 
    * I want to understand the context in which my artwork has been placed, so that I can be sure that my integrity as an artist is not compromised. 
    * I want my details and the information about my artwork to be prominent, accessible and accurate, so that I can ensure my moral rights as an artist are being respected.

</details>

---
## R5. Wireframes for multiple standard screen sizes, created using industry standard software	

<details><summary>Click to expand</summary>

[Click here to view prototype on Figma](https://www.figma.com/proto/qeHkwgWMhlNLU0kqAG7YAz/Wireframes?node-id=9%3A7&viewport=521%2C164%2C0.28764817118644714&scaling=scale-down)

Home:<br><img src="./docs/Part-A/home.png" alt="Home" width="200"/><br><br>
Map view:<br><img src="docs/Part-A/map.png" alt="Map view" width="200"/><br><br>
Search view:<br><img src="docs/Part-A/list.png" alt="Search view" width="200"/><br><br>
Artwork details:<br><img src="docs/Part-A/artwork.png" alt="Artwork details" width="200"/><br><br>
About page:<br><img src="docs/Part-A/about.png" alt="About page" width="200"/><br><br>
Administrator log in:<br><img src="docs/Part-A/login.png" alt="Administrator log in" width="200"/><br><br>
Administrator home:<br><img src="docs/Part-A/admin.png" alt="Administrator home" width="200"/><br><br>
Administrator add/edit artwork:<br><img src="docs/Part-A/add.png" alt="Administrator add/edit artwork" width="200"/><br><br>
</details>

---
## R6. Screenshots of your Trello board throughout the duration of the project	

<details><summary>Click to expand</summary>

Week 1
![Screenshot 1](./docs/Part-A/Trello_Screenshots/ScrnSht_1.png)

Week 2
![Screenshot 2](./docs/Part-A/Trello_Screenshots/ScrnSht_2.png)

Week 3
![Screenshot 3](./docs/Part-A/Trello_Screenshots/ScrnSht_3.png)

Week 4
![Screenshot 4](./docs/Part-A/Trello_Screenshots/ScrnSht_4.png)
![Screenshot 5](./docs/Part-A/Trello_Screenshots/ScrnSht_5.png)
</details>

</details>