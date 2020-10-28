# SPS-5586-Movie-ticketing-bot

# "By Dr.C.V.Guru Rao" 

[My repository link](https://github.com/SmartPracticeschool/SPS-5586-Movie-ticketing-bot.git "Movie Ticketing Bot")

## Movie ticketing bot

This repository is to present the development of a project-build-a-thon Movie ticketing bot that is capable of booking movie tickets on viewer choosen show timings, inform the viewer on availability of seats together with their price and confirm booking of tickets using Watson Assistant Service and integrate it Node-Red Application

## Prerequisites  

* One must have an IBM Academic Initiative/Cloud account. The account is free and provides access to everything you need to develop, track, plan, and deploy apps. The account requires an IBMid. 

* IBM Academic Initiative/Cloud account must have at least 8 GB of runtime and container memory, plus access to provision up to 10 services.

* It need a clone of this GitHub repository, as one might need some of the files to expedite the work.

* To develop on the movie ticketing bot to run locally or on IBM Cloud, one must be familiar with Watson Assistant and Node Red app.

## Steps to Implement Movie ticketing bot

##__Login onto IBM Cloud Academic Initiative account__ 

![IBM Cloud Login Page](./Images/CVGR-MTB-WA-Image-44-22-10-20.png)

An IBM Cloud account - A lite account, which is granted for the purpose of project-build-a-thon, is being created at IBM Cloud    

![IBM Cloud Login Page - User name](./Images/CVGR-MTB-WA-Image-46-22-10-20.png)  

##__Create Watson Assistant service__  

1.Select Catalog found at the top right of the page

![IBM Cloud Dashboard](./Images/CVGR-MTB-WA-Image-1-20-10-20.png)

2.Click on Watson from the list of Platform services  

3.Select Watson Assistant. Enter the Service name or keep the default value and make sure to select your desired region/location, organization, and space.Select Lite for the Plan. Click on Create 

4.Watson Assistant service main page is created. Click on Launch tool  

![Watson Assistant](./Images/CVGR-MTB-WA-Image-3-19-10-20.png)

##__Create Workspace__  

1.Scroll down and click on Create a Workspace found under Get started now  

2.Click on Create assistants to Create a new workspace named Movie ticketing Bot  

![My First Assistant](./Images/CVGR-MTB-WA-Image-45-19-10-20.png)

3.This will open the workspace. Where the Intents, Entities and Dialog are defined  

![My first skill](./Images/CVGR-MTB-WA-Image-26-19-10-20.png)

##__Define Intents__

1.Under the tab Intents, click on Add intent  

2.Enter the Intent name and Description (optional) and click on Create intent  

3.Under Add user examples, add the utterances that are expected to be mentioned based on the intent and click on Add example  

![Intents](./Images/CVGR-MTB-WA-Image-5-19-10-20.png)

##__Define Entities__

1.Under the tab Entities, click on Add entity  

2.Enter the Entity name and click on Create entity  

3.Add the Value name and its corresponding Synonyms and click on Add value  

![Entities](./Images/CVGR-MTB-WA-Image-6-19-10-20.png)

4.Under System entities enable sys-date and sys-number 

![System Entities](./Images/CVGR-MTB-WA-Image-7-19-10-20.png)

##__Define Dialog Flow__

1.Click on the tab Dialog. where you will see to pre-defined nodes: Welcome and Anything else 

2.Click on the Welcome node and modify the response of the bot to greet any user  

3.Click on Add node below to add a node under the Welcome node  

4.Call the node Greetings and set the condition under If bot recognizes to #greeting.This means that, after the welcoming message,if the bot detects that the user is greeting it,it will respond with whatever is added under Then respond with: and wait for user input  

5.Create an empty node below the Greetings node and if bot recognizes @movie:(Avengers-ENGLISH) then assistant responds with the corresponding image of the movie and list of cities in which it is being screened  

6.Four such empty nodes are added in succession corresponding to each of the four movies used in this bot respectively  

7.Under the last out of five i.e., @movies:(Kotha Janta-TELUGU) another empty node is added, in which, if bot recognizes @cities then assistant responds to capture the number of seats required  

8.Next, an empty node under this node is added. In this if the bot recognizes @price then assistant reponds to display the price of the tickets the viewer is requesting for by capturing number seats required. Further, it moves to the next node after evaluating the response  

9.Another node is added under the node listed at previous step. In this node if the bot recognizes #seats then assistant responds to capture the date on which the viewer wants to watch the movie  

10.A node is created again below the node at pevious step. Here in this node if the bot recognizes @sys-date then assistant responds with displaying the show timings  

11.Then again a node under the above one is created, where if the bot recognizes #time then assistant responds to capture mobile number of the viewer  

12.Next in the sequence another node is added below to send an OTP to the mobile number if bot recognizes @sys-number  

13.Now again a node is added below to capture the mode of payment if the bot recognizes @payment  

14.Then again, Create a new node and call it Thank You, whcih acknowledges with an emoji image when #thankyou is detected  

![Dialog](./Images/CVGR-MTB-WA-Image-8-19-10-20.png)

![Dialog](./Images/CVGR-MTB-WA-Image-9-19-10-20.png)

![Dialog](./Images/CVGR-MTB-WA-Image-10-19-10-20.png)  

![Dialog](./Images/CVGR-MTB-WA-Image-11-19-10-20.png)  

![Dialog](./Images/CVGR-MTB-WA-Image-12-19-10-20.png)

##__Try Out steps of Movie Ticketing Bot__

15.Finally, Try out is succesfully used to verify  the desired result as shown below in the steps lited.  

![Try out Screen](./Images/CVGR-MTB-WA-Image-47-23-10-20.png)

![Try out Screen](./Images/CVGR-MTB-WA-Image-48-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-49-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-50-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-51-23-10-20.png)

![Try out Screen](./Images/CVGR-MTB-WA-Image-52-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-53-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-54-23-10-20.png)  

![Try out Screen](./Images/CVGR-MTB-WA-Image-55-23-10-20.png)

![Try out Screen](./Images/CVGR-MTB-WA-Image-56-23-10-20.png)

16.From the My first assiatant screen click the preview link and the Assistant preview is opened in a seperate browser  

![Skill Integration](./Images/CVGR-MTB-WA-Image-26-19-10-20.png)

![Creation of Preview Link](./Images/CVGR-MTB-WA-Image-27-19-10-20.png)  


[Watson Assistant Generated url to Create GUI](https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=eu-gb&integrationID=593d9d3c-0b77-49f7-bfc8-78fae57849f4&serviceInstanceID=2bb06dd0-a74d-45c1-931e-a3389d82c4a6 "url creted")

17.The bot greets the bookee and waits the input  

![url](./Images/CVGR-MTB-WA-Image-28-19-10-20.png)

18.When the greeting is reciprocated, the bot responds with list of movies available  

![Movie List](./Images/CVGR-MTB-WA-Image-30-19-10-20.png)

19.For a choosen movie an image is displayed and also displays a City to be selected  

![City choice](./Images/CVGR-MTB-WA-Image-32-19-10-20.png)

20.Upon selecting the city the bot responds to capture the number of seats required to book. In response to the capture of number of seats required to be booked the bot displays the price of seats requested and waits for the date on which the movie tickets are to be booked  

![Number of Seats](./Images/CVGR-MTB-WA-Image-33-19-10-20.png)

21.On accepting the date the bot reponds to enter mobile number  

![Mobile number](./Images/CVGR-MTB-WA-Image-34-19-10-20.png)

22.When the bookee enters the mobile number the bot sends an OTP to the mobile number  

23.On entering the received OTP the bot enquires the mode of payment  

24.When the payment mode is updated a message is sent to complete the payment and book the slots  

![OTP, Payment mode](./Images/CVGR-MTB-WA-Image-35-19-10-20.png)

25.Finally, bot responds with an emoji for the service it rendered  

![Emoji](./Images/CVGR-MTB-WA-Image-36-19-10-20.png)

26.From the resources page of the IBM cloud Open Node Red apllication page  

![Node Red](./Images/CVGR-MTB-WA-Image-36a-20-10-20.png)

27.Node Red application details page opened and in this page click Create under Cloud Foundry Apps  

![Node Red App](./Images/CVGR-MTB-WA-Image-37-19-10-20.png)

28.Node Red Application is opened and it contained visit url link. Click on this link to open the Node Red page after going through the settings needed  

![Node Red url](./Images/CVGR-MTB-WA-Image-38-19-10-20.png)

29.A flow is loaded into Node Red and configured to accept the input from bot  

![Node Red Flow](./Images/CVGR-MTB-NRed-Image-42-20-10-20.png)

30.Open UI of the Node Red  

31.Enter the interaction and observe the responses  

![Node Red Flow](./Images/CVGR-MTB-NRed-Image-43-20-10-20.png)

32.Finally, the bot is verified to be able to book movie tickets successfully

##__Links to YouTube Videos__  

[![IBM Watson Assistant Video](http://img.youtube.com/vi/6lRf2VYgc_c/0.jpg)](http://www.youtube.com/watch?v=6lRf2VYgc_c "IBMWA") 

[![GUI2IBMWA VIDEO](http://img.youtube.com/vi/6lRf2VYgc_c/0.jpg)](http://www.youtube.com/watch?v=6lRf2VYgc_c "GUI2IBMWA")

[![GUI2IBMNRED VIDEO](http://img.youtube.com/vi/s3nib_y_b1g/0.jpg)](http://www.youtube.com/watch?v=s3nib_y_b1g "GUI2NODERED")

##  References

1 Bot Asset Exchange (contains workspaces that can be explored)  

   + https://developer.ibm.com/code/exchanges/bots/  

2 Watson Assistant courses (to help learn about Watson Assistant features)  

+ https://developer.ibm.com/courses/all/chatbots-watson-lets-talk-national-parks/  

+ https://developer.ibm.com/courses/all/chatbots-for-good-empathetic-chatbots/  

+ https://cognitiveclass.ai/courses/how-to-build-a-chatbot/  
 
3 Watson Assistant Docs and Resources  

+ https://www.ibm.com/cloud/watson-assistant/docs-resources    

4 Bot TJ (contains fun projects to build using some hardware components)  

   + https://ibmtjbot.github.io/

