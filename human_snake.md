- [Customer Requirements:](#customer-requirements)
    - [Functional Requirements:](#functional-requirements)
    - [Performance Requirements:](#performance-requirements)
    - [Security Requirements:](#security-requirements)
    - [User interface and Usability:](#user-interface-and-usability)
- [Brief Introduction:](#brief-introduction)
- [User Guide:](#user-guide)
  - [Summary:](#summary)
  - [Login System:](#login-system)
  - [Leaderboard System:](#leaderboard-system)
  - [Playing the game:](#playing-the-game)
    - [Basic rules:](#basic-rules)
- [BOM](#bom)

</div id="customer-requirements">

# Customer Requirements:

</div id="functional-requirements">

### Functional Requirements:

* Want a “snake-like” game where people can walk around and an app will show what their current “tail” looks like  
* Multiplayer functionality, where other snakes can be “killed”   
* Login system to track individual snakes (players)  
* Steps tracker for health enthusiasts  
* Leaderboard for snakes  
* The tail should follow the player’s movements, showing the history of where they have been

### Performance Requirements:

* The length of the snake and the shape of the snake should be displayed in less than 2 seconds.  
* The system should support at least 40 players at the same time without affecting response time.  
* The server should be able to list all other players, and their positions near the logged in player

### Security Requirements:

* To ensure the Human Snake IoT game functions correctly, the mobile app must request and be granted the following permissions during gameplay including GPS, built-in accelerometer, WiFi, Cellular Data.   
* Real names will not be shared with other players, instead you will be randomly given the name of a real life snake species for the day.

### User interface and Usability:

* The user interface of the proposed smartphone application must be clear and easy to operate. The main features of the application should  include a brief welcome message, overview of core features, navigation menu, user account information, and quick start button.   
* Real-time display of game progress. During the game, the user will have access to the map that shows the location of each player, allowing users to see their relative distance and movement direction in relation to other team members, and make adjustments accordingly. 


# Brief Introduction:

The human snake is an interesting application that transforms the class “snake” game into a real-world, multiplayer experience using smartphones as the primary sensor and communication platform. Utilizing the advanced capabilities of smartphones, including GPS, built-in sensor, and equipped communication technology,  to create a dynamic and engaging game where players physically move to control their virtual “snake”. 

Upon launching the app for the first time, users are prompted to log in or register with a unique username and password, ensuring personalized tracking and secure access. After granting permission for the app to access their location data, users can view the number of online players within their area, representing potential participants for future games. Players have the option to either host their own game or join an existing one. When a user joins a game, the app initializes a virtual snake with a 50-foot tail that dynamically follows the player’s movements. As participants navigate their surroundings, the app tracks their total distance traveled and updates the tail’s position in real time. Players can interact by “killing” opposing snakes, which extends their own tail by 10 feet and elevates their ranking on a localized leaderboard that resets daily to maintain a balanced competitive environment. 

Designed with a user-friendly interface, the Human Snake app features a clear welcome message, an intuitive navigation menu, and real-time visualizations of game progress. The map interface displays each player’s location, relative distance, and movement direction, allowing users to make informed adjustments to stay connected with their team. 

Beyond the core gameplay mechanics, the project emphasizes health and social benefits by integrating a steps tracker that encourages physical activity, promoting a healthier lifestyle among players. The multiplayer aspect provides numerous social opportunities, enabling participants to connect, compete, and collaborate within their local community. Security and privacy are paramount, with robust measures in place to protect user data and ensure anonymity by assigning each player a random selected snake species name instead of their real identities. 

By blending physical movement with digital interaction, the Human Snake not only offers a unique and entertaining gaming experience but also highlights the potential of IoT technology in enhancing traditional games. The detailed User Guide and Customer Requirements sections further outline the necessary functionalities, performance standards, and security measures essential for the successful implementation and operation of the Human Snake game. 

# User Guide:

## Summary:

Open the app and login or register with a unique username and a password.  
It will then ask for permission to use your location data for the game, select okay.  
It will then begin creating your snake, with a tail 50 ft in length starting from the location you began in, and following behind you. The app will not only track your total distance while playing, but also move your tail behind you and show other players who are playing in your area. Depending on how many other snakes you kill, it will show you on a leaderboard within the app. 

## Login System:

Logins will require a valid email, which has not been used before and a password to go with it. The login page will also have a “forgot my password” button in case you forgot what you set it to, and you can change it by sending a code to your email and entering the code within the application. 

## Leaderboard System:

The leaderboard system will not be global, instead it will pull from all of the snakes in your area (approximately ten mile radius) and display them in the leaderboard. They will be the snakes you will see on the map as well when you are playing the game. Points will reset at the end of the day (12AM in your local time) to avoid someone from being the boss for a ridiculous amount of time. 

## Playing the game:

### Basic rules:

* Killing an opposing snake will increase the length of your own tail by 10ft.  
* Increasing or decreasing your speed will not change the length of your tail, that remains constant. This will avoid people on bikes or in cars from having an unfair advantage. The advantage would instead go to pedestrians, as they are putting in the most caloric effort.  
* You cannot be killed by the same snake while your tail remains within its tail. This avoids people walking back and forth and accidentally (or intentionally) giving another snake a ridiculous amount of points.   
* There is a 30 second cooldown period on killing a snake, you cannot kill the same snake again until that period is over (but they can kill you).  
* If a single snake has a majority of the points ( \< 50% of all points in your play area) they will be considered a boss, and all snakes will get double points for killing them. However the boss’s tail is also twice as long.

You will get a notification alert on your device when you are 100ft away from another snake to avoid accidental collisions. You will also get alerts when you have killed, and when you have been killed.

# BOM

The cost of this is mostly in development time, requiring no special equipment as the players use their existing phones as the nodes in the network. There will be a server required, but it can be hosted on Azure’s student plan at no cost.