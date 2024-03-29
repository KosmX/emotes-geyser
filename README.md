# emotes-geyser  
## Just a standard Emotecraft-GeyserMC setup  

## Currently in beta:
> Latest geyser supports emote event, to unleas its potencial, please install this extension: [KosmX/geyser-emote-extension](https://github.com/KosmX/geyser-emote-extension)  

You can use any 2.2 emotecraft build.  
NOTE: Forge doesn't support Geyser clients. The issue is with Forge. If Forge server works for you, DM me!

## Usage  

Copy the content of the `.minecraft` folder into your minecraft server folder.  

## Current state of this repo

You can follow the changes here:  
https://docs.google.com/spreadsheets/d/16pRqKIPl-y2mlJQCgfiGmVWN-B_xXoll-CH8bGodYh0/edit?usp=sharing

## How and why? 
  

__BE__(Bedrock Edition) does not support custom emotes, but I can ask it to play *any* built-in emote.  
Downloaded marketplace content is encrypted, I can not load __BE__ emotes in __JE__(Java Edition).  
  
Emote mapping is needed: 
`config/emotecraft_emote_map.json`  
It will pair __BE__ emotes and __JE__ emotes.  
You can find BE emote UUIDs here:  
[GitHub.com/JustTalDevelops/bedrock-emotes](https://github.com/JustTalDevelops/bedrock-emotes)  
__JE__ emote UUID in the json:
```json
	"author": "KosmX",
	"description": "Like say Hi!",
	"uuid": "33b912f8-0aa0-45e6-a2d4-9b5677e6f35c", //<--------------
	"emote":{
        (...)
```
//TODO emotecraft binary howto

### Mapping file

```json
{
  "bedrock-emote": "java-emote",
  "4c8ae710-df2e-47cd-814d-cc7bf21a3d67": "33b912f8-0aa0-45e6-a2d4-9b5677e6f35c",
  "9a469a61-c83b-4ba9-b507-bdbe64430582": "96506a5e-a69c-4a18-9add-d43dfd272fa6",
  (...)
}
```
The first line in the code above, is **only** a comment. You can remove it, changing it won't do anything.  

Emotecraft will ignore every line, what can not be interpreted as a **uuid** pair. Feel free to add comment lines.  

**If you use custom emotes** do not forget to add those to the server.
`server-folder/emotes/*`  
