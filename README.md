# Personalised-Voice-Assistant
##CODE:'=
```

#------------------------------------Modules------------------------------------#
import speech_recognition as sr
import pyaudio
import random
import webbrowser
import pyttsx3
from pynput.keyboard import Key,Controller
import urllib.request
from tkinter import *
#import mysql.connector as ms
#from PIL import ImageTk,Image
#--------------------------------------coding-------------------------------------#
k=Controller()
while True:   
 r=sr.Recognizer()

 try:
  with sr.Microphone()as source:
        
    audio=r.listen(source)
    c=r.recognize_google(audio)
    c=c.lower()
    
    engine = pyttsx3.init()


    if 'sunday' in c:
        print(c)
    
        if c=='sunday': 
          a='yes boss'
          b='at your service'
          d='i am online boss'
          e='here to help'
          r=random.randint(0,3)
          if r==0:
           engine.say('yes boss')
           engine.runAndWait()
          elif r==1:
           engine.say('at your service')
           engine.runAndWait()
          elif r==2:
           engine.say('i am online boss')
           engine.runAndWait()
          elif r==3:
           engine.say('here to help')
           engine.runAndWait() 
          #k.press(Key.space)
          #k.release(Key.space)
       
      
          audio=r.listen(source)
          p=r.recognize_google(audio)
          p=p.lower()
        
        
        if 'youtube' in c:
            
           if 'search' in c:
              
            engine.say('yes boss')
            engine.runAndWait()
            
            i='youtube and search'
            m='sunday search in youtube'
            if i in c:
              x=c.partition(i)
              h=x[2]

            elif m in c:
              y=c.partition(m)
              h=y[2]
            webbrowser.open("https://www.youtube.com/results?search_query="+h)
             

           elif 'subscription' in c: 
            engine.say('yes boss')
            engine.runAndWait()
            webbrowser.open("https://www.youtube.com/feed/subscriptions")

           if 'youtube' in c:
             engine.say('yes boss')
             engine.runAndWait()  
             webbrowser.open("https://www.youtube.com")
     
        elif 'insta' in c:
             engine.say('yes boss')
             engine.runAndWait()
             webbrowser.open("https://www.instagram.com")
        elif 'music' in c:
           
           if 'music and search' in c:
             engine.say('yes boss')
             engine.runAndWait()
             i='sunday open music and search'
             if i in c:
                x=c.partition(i)
                h=x[2]
                webbrowser.open("https://music.youtube.com/search?q="+h)
                #k.press(Key.space)
                #k.release(Key.space)
           


             
           elif 'english songs' in c:
                    
                    engine.say('yes boss')
                    engine.runAndWait()
                    webbrowser.open("https://music.youtube.com/watch?v=zVB2y513-SQ&list=PL7EkpAjPakGobn4-Q-B4V_qiaqBkLAOPA")
                    k.press(Key.space)
                    k.release(Key.space)
                    
           elif 'ncs songs' in c:
                     
                     engine.say('yes boss')
                     engine.runAndWait()
                     webbrowser.open("https://music.youtube.com/watch?v=bLZHcnuqscU&list=PL7EkpAjPakGoCZ7tvPJG62UpyPu6rxxA5")
                     k.press(Key.space)
                     k.release(Key.space)
           elif 'music' in c: 
             engine.say('yes boss')
             engine.runAndWait() 
             webbrowser.open("https://music.youtube.com")
           
        elif 'search' in c:
           engine.say('yes boss')
           engine.runAndWait()
           i='sunday search'
           if i in c:
              x=c.partition(i)
              h=x[2]
              webbrowser.open("https://www.google.com/search?q="+h)

        elif '+' in c:
              engine.say('ok boss')
              engine.runAndWait()
            
            
              x=c.split()
              print(x)
              for i in x:
                  
                  
                 #if i.isdigit():
                 if type(i) is int: 
                    l=[]
                    l.append(i)
                    engine.say('k boss')
                    engine.runAndWait()
                    
                 for z in l:
                     m=m+z
                    
               
                 print(m)
                    
        elif 'play the song' in c:
                        engine.say('yes boss')
                        engine.runAndWait()
                        k.press(Key.space)
                        k.release(Key.space)
                        
        elif 'pass the song' in c:
                        engine.say('yes boss')
                        engine.runAndWait()
                        k.press(Key.space)
                        k.release(Key.space)
                        
        elif 'next song' in c:
                        with k.pressed(Key.shift):
                           k.press('n')
                           k.release('n')

        elif 'previous song'in c:
                        with k.pressed(Key.shift):
                            k.press('p')
                            k.release('p')
                           
        elif 'deactivate' in c:
             r.pause_threshold=1
             engine.say('it was nice ,serving you boss')
             engine.runAndWait()
             break

        elif 'hi' or 'hello' in c:
             r.pause_threshold=1
             engine.say('hi,boss')
             engine.runAndWait()
        else:
         engine = pyttsx3.init() 
         engine.say('i am unable to understand what you told  ,  boss  ,please say it again')
         engine.runAndWait()

    
    else:
       if 'deactivate' in c:
             engine = pyttsx3.init() 
             r.pause_threshold=1
             engine.say('it was nice ,serving you boss')
             engine.runAndWait()
             break     
   

 except:
    pass


```
