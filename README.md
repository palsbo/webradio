# Webradio for Synology
Webradio with node.js server and url broadcast to esp8266 clients
The Node.js server and client can also be used on any other system architecture.
Use the folder 'webradio/package' as base folder for the node application.

##	Server:
The node.js server is a webserver with webpages to select a live stream url.
The server uses Websocket for variable data to/from clients.
When the server receive a stream url, it is broadcasted using Websocket as a JSON message like this:

	{ 'url' : '<http://livestreame.com>' }

The server also broadcasts the following information:
-	StreamTitle
-	samplerate
-	britrate
-	channels
These values are also broadcasted as JSON messages.

##	Web client:
The client can be used as a webradio and for selecting stations.

##	ESP8266 listener:
Using a ESP8266 as a listener, it can be connected to an amplifier.
By adding a I2S DAC module, the quality improves and the module can provide stereo.



