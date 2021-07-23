# Upload-YT-Video-Bot
***The script uses Google's YouTube Data API to upload the video on Youtube Programatically.***

## Setup

Clone the script

**Use**:  git clone https://github.com/Prabhakar-MishraCS/Upload-YT-Video-Bot.git

Install the requirements with pip
  **pip install google-auth**

## YouTube API Setup
You need to first create an account on Google Cloud Platform in-order to use the YouTube Data API v3 (which is required to programatically upload videos to YouTube). Follow these steps to do so:

1. Create an account on the Google Developers Console
2. Register a new app there
3. Enable the Youtube API (APIs & Services -> Enable APIs and Services)
4. Go to APIs & Services -> OAuth Consent screen.
5. Configure your App name, developer email, etc and go to Scopes
6. Add the scope 'youtube.upload', and then 'Save and Continue'
7. Add the email address of the channel in 'Test Users' and Save.
8. Create Client ID (APIs & Services -> Credentials -> Create Credentials), select 'Oauth client ID', select type 'Web application'
9. Add an 'Authorized redirect URI' of 'http://localhost:8080/oauth2callback'
10. Download the client secrets JSON file (click download icon next to newly created client ID) and save it as file client_secrets.json in the same directory as the script.


### Run
First run config.py to authenticate your channel with YouTube API. This will create a file named credentials.txt in the same directory. You only need to run this once. python config.py

If your video belongs to any category other than Education, you need to mention the appropriate category ID. You can find the list of categoy IDs [here](https://gist.github.com/dgp/1b24bf2961521bd75d6c).

You can also use a constant description for all your uploads by changing the text in constdesc.txt file. The credits text will be automatically appended to the description while uploading the video. You can also specify hashtags to include in the description.


***Finally!***

**python ytupload_util.py**

Fill the required inputs (video file, title, description, tags, privacy status) and the video will be **uploaded!**
