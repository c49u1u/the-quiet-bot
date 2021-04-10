# The Quiet Bot
## The Discord Bot That Tells You To STFU When You Talk In VC
---
---
### Some Code Explaination
##### Joins VC That User Is In:
```javascript
client.on('message', async message => {
	if (message.member.voice.channel){
		message.member.voice.channel.join();
	}
});
```
##### Broken Down:
```javascript
client.on('message', async message => { //This is what listens for messages. 
//"client.on" is a function to declare what happens on a certain event. For example: "message" (i think. idk im just a softawre dev :/)
//In this case, it is made to run no matter what the message says.

	if (message.member.voice.channel){ //Finds if the user is in a voice channel.
  //"message.member" meaning the member who sent the message.
  //"voice.channel" meaning the voice channel the member is in (if they are in one).
  
		message.member.voice.channel.join(); //Joins the voice channel using the "join()" function brought by Discord.js.
	}
});
```
---
##### DM User When They Start Speaking (telling them to stfu):
```javascript
client.on('guildMemberSpeaking', function(member, speaking){
	if (member.speaking = true){
		member.send('STFU')
	}
})
```
##### Broken Down:
```javascript
client.on('guildMemberSpeaking', function(member, speaking){ //Detects when user is speaking (green circle will appear around user avatar when speaking)
//"client.on" i already explained, loser.
//"guildMemberSpeaking" is one of the events involving voiceState blah blah blah its a boolean data type

	if (member.speaking = true){ //its a bit obvious but this if statement detects if user speaking is true
  
		member.send('STFU') //sends dm to user saying stfu
	}
})
```
##### ur welcomes for the code explaination my guy -c49u1u<3
