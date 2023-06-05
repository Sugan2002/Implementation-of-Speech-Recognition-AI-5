### EXPERIMENT 5
### DATE : 18.05.2023
# <p align="center"> Implementation-of-Speech-Recognition </P> 

## Aim:
 Construct a python program to implement speech recognition.
## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook
## Algorithm:
Step 1:Import the speech_recognition module as sr.<br>
Step 2:Assign a string variable "file" with the name of the audio file that you want to transcribe.<br>
Step 3:Create an instance of the Recognizer class called "r".<br>
Step 4:Use the AudioFile() method of sr to create an AudioFile object with the audio file name passed as an argument.<br>
Step 5:Use the record() method of r to read the audio data from the AudioFile object and store it in the variable "audio".<br>
Step 6:Use the recognize_google() method of r to transcribe the audio data stored in the "audio" variable.<br>
Step 7:Print the transcribed text on the console if the transcribe process was successful.<br>
Step 8:Handle any potential errors during the transcribing process. If the audio is not clear, print "not clear". If there's an error while trying to retrieve the transcribed text from the Google speech recognizer, print "Couldnt get results from google speech recognizer".<br>

## Program:

```python

import speech_recognition as sr
file = "audio_file.wav"
r = sr.Recognizer()

try:
    with sr.AudioFile(file) as source:
         audio = r.record(source)
    transcribed_text = r.recognize_google(audio)
         print("Transcribed Text:")
    print(transcribed_text)

except sr.UnknownValueError:
    print("Audio is not clear.")

except sr.RequestError:
    print("Couldn't get results from Google Speech Recognizer.")


```
## Output:

![image](https://github.com/Sugan2002/Implementation-of-Speech-Recognition-AI-5/assets/77089743/fd42b791-be6c-4a35-b388-058ad508487e)

## Result:
     Thus, we've implemented speech recognition successfully.
