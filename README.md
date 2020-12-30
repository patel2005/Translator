# Translator
A translator consisting of twelve languages and a text to speech
'''
Veeraj Patel
11/29/2020
Codeathon
TTS-Translator
'''

# use pip install google_trans_new
# google translate module 
from google_trans_new import google_translator  
# text to speech module
from gtts import gTTS

def main():
# welcome
  print("Hello!")

# language selection  
  print("Please enter the number of the language you what to hear")
  print("""
        1. English      7. Arabic        
        2. Spanish      8. Afrikaans
        3. French       9. Vietnamese
        4. Chinese      10. Swahili
        5. Hindi        11. Russian
        6. Korean       12. Italian
          """)  
  language = input("Enter here: ")

#TRANSLATOR

  # english
  if(language == '1'):
    translator = google_translator()
    speak = input("Enter what you want to hear: ") 
    conv = translator.translate(speak,lang_tgt='en')  # convert the text the user entered in speech to English
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")
    
    # put the new text into an mp3
    speech = gTTS(text = conv, lang = 'en', slow = False )
    speech.save('text.mp3')
    
  # spanish
  elif(language == '2'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='es')  # convert the text the user entered in speech to Spanish
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang = 'es', slow = False )
    speech.save('text.mp3')
 
  # french
  elif(language == '3'):
    
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='fr')  # convert the text the user entered in speech to French 
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3 
    speech = gTTS(text =  conv, lang = 'fr', slow = False )
    speech.save('text.mp3')        

  # Chinese
  elif(language == '4'):
    
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='zh-CN')  # convert the text the user entered in speech to Chinese
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang = 'zh-CN', slow = False )
    speech.save('text.mp3')

  # Hindi   
  elif(language == '5'):
    
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='hi')  # convert the text the user entered in speech to Hindi 
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase 
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang = 'hi', slow = False )
    speech.save('text.mp3')     

  # Korean
  elif(language == '6'):
    
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='ko')  # convert the text the user entered in speech to Korean
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang = 'ko', slow = False )
    speech.save('text.mp3')  

  # Arabic
  elif(language == '7'):

    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='ar')  # convert the text the user entered in speech to Arabic
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang ='ar', slow = False )
    speech.save('text.mp3')


  # Afrikaans
  elif(language == '8'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='af')  # convert the text the user entered in speech to Afrikaans
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3
    speech = gTTS(text = conv, lang = 'af', slow = False )
    speech.save('text.mp3')


  # Vietnamese
  elif(language == '9'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='vi') # convert the text the user entered in speech to Vietnamese
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3 
    speech = gTTS(text = conv, lang = 'vi', slow = False )
    speech.save('text.mp3')


  # Swahili
  elif(language == '10'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='sw')  # convert the text the user entered in speech to Swahili
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")
      
    # put the new text into an mp3 
    speech = gTTS(text = conv, lang = 'sw', slow = False )
    speech.save('text.mp3')


  # Russian
  elif(language == '11'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='ru')  # convert the text the user entered in speech to Russian
    lw = conv.casefold() # make the trans text lowercase
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3 
    speech = gTTS(text = conv, lang = 'ru', slow = False )
    speech.save('text.mp3')


  # Italian
  elif(language == '12'):
    translator = google_translator()
    speak = input("Type what you want to hear: ")
    conv = translator.translate(speak,lang_tgt='it')  # convert the text the user entered in speech to Italian
    lw = conv.casefold() # make the trans text lowercase  
    spklw = speak.casefold() # make the speak text lowercase
    bordersList2 = ["\t\t", spklw, "\t\t\t\t------>>>>\t\t\t\t","\t\t", lw]
    print("")
    for x in bordersList2:
      print(x,end="")

    # put the new text into an mp3  
    speech = gTTS(text = conv, lang = 'it', slow = False )
    speech.save('text.mp3')

  # give an error if user enters something not on the list (make it red)
  else:
    print("\033[1;31;47m ERROR: enter correct option")

if(__name__=="__main__"):
  main()
