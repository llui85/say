# say.py
 
**🟥🟥🟥  Note: This is in development and currently unfinished.  🟥🟥🟥**
  
An distributed speech synthesis network for macOS. This hosts a mini-network which allows you to push out a text-to-speech utterances to many computers at once, using [`say`](https://ss64.com/osx/say.html).

## Types

```json
{
  "_type": "Request",
  "action": "send_utterance",
  "parameters": {},
  "scriptVersion": "1.0.2",
}
```
```json
{
  "_type": "Response",
  "errorStatus": true,
  "errorMessage": "Target volume out of range",
  "errorId": "volume_out_of_range",
  "scriptVersion": "1.0.2",
}
```
```json
{
  "_type": "Utterance",
  "text": "Hello everybody!",
  "time": "now",
  "preferredVoice": "Cellos",
  "allowVoiceFallback": true
}
```
```json
{
  "_type": "Voice",
  "name": "Cellos"
}
```
```json
{
  "_type": "ConnectionType",
  "ethernet": true,
  "wifi": false
}
```
```json
{
  "_type": "Device",
  "hostname": "Admin's Macbook Air",
  "osVersion": "11.3.2",
  "ip": "192.168.1.5",
  "connectionTypes": ConnectionType,
  "voices": [Voice],
  "lastConnectionTime": 12182341
}
```

## Components

### Socket Server

### HTTP Server

A simple HTTP Server to display connected device status, and to push utterances out to the network. By default it is accessible on port `19034`, however this can be changed if necessary.
