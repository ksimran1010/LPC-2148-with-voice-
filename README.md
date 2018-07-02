# LPC-2148-with-voice-
This file will provide you a step by step guide on how to add a voice/audio to any microcontroller code with a DAC enabled 
feel free to copy/contribute to this project or its resources .If needed contact me on ceasaze@gmail.com

In this example I am using LPC 2148 ARM 7 based microcontroller which is a part of blueboard development board (https://i1.wp.com/www.scienceprog.com/wp-content/uploads/2011/11/Blueboard.jpg) iam using this because it comes with built-in audio  pre - amplifier circuit.you can use same method 
-----------------------------------------------------------------------------------------------------------------
pre-requisites - 
1. LPC 2148 blueboard development board
2. a wav to c code converter software (provided with this repo)
3. a mp3 to wav converter(i recomend you to use an online version -https://audio.online-convert.com/convert-to-wav)5
4. note that a microcontroller has limited amount of rom in which it stores the code so you shoul make this wav/mp3 file as short as possible ,use compressing softwares to compress mp3 file before converting it to 
_________________________________________________________________________________________________________________

step 1 - 
 first we need to decide what is needed to be in the audio. if it is some sentence or a word ,use a text to speech converter which will output a mp3 file (eg - you can use this site for free- http://www.fromtexttospeech.com/)
 
step 2 - 
take this mp3 file and compress it (not exceeding 500kb).now we need to convert this mp3 file into a wav file (PCM formatted)
i recommend you to use this online service -https://audio.online-convert.com/convert-to-wav with following presets 
Change bit resolution: 8 bit 
Change sampling rate:  1000hz- 16000hz (higher the sampling rate larger the file size and better is the audio quality)
Change audio channels: mono(if you are using single speaker)
PCM format- 8 bit unsigned 

step 3
as soon as we get our wav file , convert it into a text file which is actually a c code containing an array of unigned integers. this is done by using special software provided in this link - https://drive.google.com/open?id=1eeYeCWTJHScqgWgbVp-thuadzSjZrD69 (this software is courtsey of - http://ccgi.cjseymour.plus.com/wavtocode/wavtocode.html) feel free to use this software since it is an open source BSD License based version.

step 4 -
copy the obtained values in the sound array as shown in the reference c program in the reporitory and compile the code and burn the hex file 

you can make this project as complex as possible as voice commands will open ton of new possiblities for your project 


 -------enjoy
