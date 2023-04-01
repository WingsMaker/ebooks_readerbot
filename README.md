# ebooks_readerbot
A telegram bot shares the list of ebooks with URL, reader can clicks on the link to read the ebooks file.

![image](https://user-images.githubusercontent.com/32192638/229261608-8df4dd8e-6904-4b3b-9532-604fa530229e.png)

Example of above ebook being clicked

![image](https://user-images.githubusercontent.com/32192638/229261705-28950827-29db-426d-909d-00cfffd3b1d5.png)


# Requirements
- Google Drive with a folder for eBooks
- Telegram chatbot token, see https://t.me/BotFather

# Getting Started - Google App Script Project
[1] Goto https://script.google.com/home 

Click "New Project" 

![image](https://user-images.githubusercontent.com/32192638/229261975-fa19519d-0a10-4e20-9642-065f30de4679.png)


[2] Rename the project

Click on the "Untitled project" to rename the project as something else. Example, "Ebooks bot".

![image](https://user-images.githubusercontent.com/32192638/229262072-5c90f86e-3459-42f5-b283-120079de578a.png)


[3] Write the scripts, copy paste from below template url :

https://raw.githubusercontent.com/WingsMaker/ebooks_readerbot/main/ebooks_readerbot.txt

![image](https://user-images.githubusercontent.com/32192638/229261805-e614d884-bfe5-4146-8c92-fccee8509eb1.png)

[4] Deploy as google web app

In the Google App Script project, go to "Publish" in the top navigation bar. 
Under "Deploy as web app", select "Deploy". This will open a pop-up window. 
Your web app URL will be listed in the "Current web app URL" field.

Click on the "Deploy - New Deployment"

![image](https://user-images.githubusercontent.com/32192638/209758084-a48fdfd0-4eb8-45be-af04-1642c3c05ed8.png)

Click "Select type - Web App"

![image](https://user-images.githubusercontent.com/32192638/209758240-b3d00b5c-09de-4355-be1d-b6193269409f.png)

Fill in the form and click "Deploy".
( for more see https://www.youtube.com/watch?v=-AlstV1PAaA )

![image](https://user-images.githubusercontent.com/32192638/209758768-29dda612-80c7-425e-8a39-e3e80d2fe5bc.png)

Copy the web app url to the clipboard for later use.

[5] Update the values of webhook in the script.

Change the value of statement, paste the url address into here.

var webhook = "___your web app url__";

[6] Update the values of token in the script.

Find your Telegram chatbot token by logging into the BotFather in Telegram, selecting your bot, 
and clicking the "API Token" button.
( see https://www.youtube.com/watch?v=aNmRNjME6mE )

Change the value of statement, paste the bot token into here.

var token = "__your telegram bot token____";

[7] Update the values of FOLDER_NAME in the script.

If your ebooks in located at the "eBooks" folder in the google drive, leave it alone.
Otherwise, update the value of FOLDER_NAME.

var FOLDER_NAME = "eBooks"; // assuming there is a folder called eBooks in your google drive.

[8] Save the script and REDO the deployment process in step 4 

since the code has been changed, need to udpate the value of webhook in [7].

[9] Run the "setWebhook" function for only once to make sure actual telegram bot 
able to callback this google web app.

![image](https://user-images.githubusercontent.com/32192638/229262318-1d1e0980-745b-4362-8363-200e6848be5e.png)

![image](https://user-images.githubusercontent.com/32192638/209759943-7c559c72-9a68-4b45-a864-639a3b9e11e6.png)

Your telegram bot is ready !
