# Terminal Chat
This is a very simple terminal chat application, it contains both the server and client code.  
The package has to be installed globally, by using ```npm i -g simple-terminal-chat```, to be able to use it!

## Server
To run the server just run ```stc-server -p 3000``` in a terminal

### Arguments
- ```-p, --port``` -> the port on which the server will run (required)

## Client
To run the client, run (e.g.) ```stc-client -i 127.0.0.1 -n nick -p 3000 -c test -h #FFAAFF -s``` in a terminal

### Arguments
- ```-i, --ip``` -> the ip-address or domain of the server (required, e.g. 'localhost', 'chat.example.com')
- ```-n, --nickname``` -> your desired nickname (required)
- ```-p, --port``` -> the port on which the chat server is running (optional, defaults to no port)
- ```-c, --chat``` -> the name of the chat that you would like to join (optional, defaults to 'general')
- ```-h, --hex``` -> the hex of the color of your name in chat (optional, defaults to #FF4500)
- ```-s, --insecure``` -> whether the connection is to be insecure or not, http vs https (optional, defaults to https)

### Commands
While you're in a chat, you can use the following commands:
- ```/chat <chatname>``` -> leaves the current chat and joins a chat with that chat name
- ```/color <color>``` -> changes your name's color to the chosen color
- ```/nickname <nickname>``` -> changes your nickname to the chosen nickname
- ```/list-chats``` -> lists the available chats on the server
- ```/list-users``` -> lists the users in a chat
- ```/exit``` -> exits the application (cleaner than CTRL+C)

## Docker
If you would like to run the application in a docker container, use the following commands:  
1. ```docker pull mithraicmagic/simple-terminal-chat-server:latest```
2. ```docker run --restart unless-stopped -d -p 4500:4500 --name stc mithraicmagic/simple-terminal-chat-server```

## TODO
- Passwords for chats
- End-to-end encryption
