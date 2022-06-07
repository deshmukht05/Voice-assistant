# Voice-assistant
Code for voice assistant.

import pyttsx3 #pip install pyttsx3
import wikipedia #pip install browser

#let name of our assitance be 'Siri'
siri = pyttsx3.init()
voices = siri.getProperty('voices')
siri.setProperty('voice', voices[2].id)
siri.say('Hello I am Siri, how may I help you')
siri.runAndWait()  #for female voice
siri.setProperty('rate', 175)


In = input("Search Wikipedia/Google: ")
result = wikipedia.summary(In, sentences = 2)
siri.say("According to wikipedia")
print(result)
siri.say(result)
siri.say("Thank you for using me")
siri.runAndWait()
