# Whatsapp ChatBot

In this, we're deploying a whatsapp chat bot to automatically reply to text message using if-else conditions as soon as message is recieved.  

## Features 

- Automatically replying a message

## Technology

- Python
- Flask
- Twilio
- ngrok


### Step 1 - Creating a Virtual Environment

Create a seperate directory, in which wr're going to create our virtual enviornment. You can learn to create a virtual env from [https://docs.python.org/3/tutorial/venv.html].

run following commands(Windows)
```sh
$ mkdir whatsappChatBot
$ cd whatsappChatBot
$ python3 -m venv auto-reply-bot
$ auto-reply-bot\Scripts\activate
(auto-reply-bot) $ pip install twilio flask requests
```

### Step 2 - Create Python Bot

We'll create a flask app to run our bot.
Create a folder in whatsappChatBot dir named "Replier" and add a new pyhton file "main.py".

Write the code written in Replier/main.py of this repository.

### Step 3 - Testing our Bot

first install ngrok in your system or virtual env (for reference- https://ngrok.com/)
It'll help us to create a temporary url for our localhost.

run command
```sh
ngrok http 4000
```

Now copy the url next to the forwarding and add the /bot in it.
Now paste it in https://console.twilio.com/us1/develop/sms/settings/whatsapp-sandbox?frameUrl=%2Fconsole%2Fsms%2Fwhatsapp%2Fsandbox%3Fx-target-region%3Dus1
where it says "WHEN A MESSAGE COMES IN"

It'll look something like this - 
```sh
"WHEN A MESSAGE COMES IN" : https://e0cf-117-203-28-7.in.ngrok.io/bot
```
