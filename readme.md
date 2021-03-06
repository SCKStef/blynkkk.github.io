#How Blynk Works
>Scheme

#Getting Started


###Download all the ingridients
**Blynk App for iOS or Android:** <br> <br> 
[<img src="http://static1.squarespace.com/static/54765ba7e4b0d055ee0b47a6/t/55515fd0e4b08237a78598e2/1431396305454/?format=500w" alt="Drawing" style=" width: 150px;"/>](https://itunes.apple.com/us/app/blynk-control-arduino-raspberry/id808760481?ls=1&mt=8)  &nbsp; &nbsp; &nbsp; &nbsp;     [<img src="http://static1.squarespace.com/static/54765ba7e4b0d055ee0b47a6/t/55515fe8e4b08237a785995e/1431396357648/?format=750w" alt="Drawing" style=" width: 200px;"/>](https://play.google.com/store/apps/details?id=cc.blynk)

**Install Blynk Library:** <br><br>
[Download Blynk Library >](https://github.com/blynkkk/blynk-library/archive/v0.2.1.zip)

In case you forgot how to install Arduino libraries: check [here](http://www.arduino.cc/en/guide/libraries).  We are also good friends of **[codebender](https://codebender.cc/example/BlynkSimpleEthernet/GettingStarted:BlynkBlink)** - you can upload Blynk sketches directly from your browser.

###Blink With Blynk 

Let's start with something easy: turn LED connected to your hardware ON and OFF with the Blynk App

Use this wiring scheme to connect LED to your Hardware:

<img src="http://faberfun.com/wp-content/uploads/2013/08/Blink-LED-using-Arduino-uno.jpg" alt="Drawing" style="width: 250px;"/>

### Create Blynk Account In The App
>Screenshot


### Get Auth Token
**Auth Token** is used to connect your Arduino or other board to your smartphone. Every new project you create will have an Auth Token. 

>Screenshot / animation

It's very convenient to send it over E-mail. If you press E-mail button – token will be sent to the e-mail address you used for registration. If you have a good memory - you can memorize it ;) or tap the number and it will be copied to the clipboard.

### Choose your hardware
Select the hardware you are building project on.
>Screenshot



#Let's get online
You know that **Blynk works over the Internet**, right? (Bluetooth LE is on the way) 

Blynk works with almost anything, check the [full list of supported hardware]()

Before you start Blynking, you need to understand how you will connect to the Internet. May be it's an Ethernet Shield for Arduino, or may be your hardware is already internet-enabled (e.g. Spark Core). 

We've prepared sketches that will get your microcomputer online. Open the example sketch according to your device or shield. If you are using **codebender** - find the example in the list

> Screenshot

Find next line in the code:

``` 
char auth[] = "YourAuthToken";

```

Change it by putting your Auth Token inside curly brackets:

``` 
char auth[] = "123456789abcdefghijk0987654321";

```

Upload sketch to the board and open Serial Terminal. Wait until you see something like this: 

``` 
Your IP is 192.168.0.11
Connecting...
Blynk connected!

```
**Congratulations! You are all set to Blynk!**

###Connect over USB,  and others

* You can play with Blynk directly over USB. It's a bit tricky for newbies, but if you follow these [USB instructions](link) you'll succeed for sure.

###Raspberry Pi, Spark Core
* **Spark Core** owners: check [here]()
* **Raspberry Pi** eaters: [here]() 


# Set up Blynk project

Open your project in the app. It's empty now, so let's add a Button. Just tap anywhere on empty space - Widget Box will open. Choose the Button Widget.

> Screenshot

Hold and drag it to reposition

> Screenshot

Tap on the widget to get to it's settings  

> Screenshot

The most important parameter to set is **PIN** . List of pins reflects physical pins defined by your hardware. If your LED is connected to Digital Pin 10 - then select **D10** (**D** - stands for **D**igital). Virtual pins are described [here]().    

> Illustration showing how Physical PIN is connected to Pin in the APP.

When you are done with the Settings - press **PLAY** button. This will switch you from EDIT mode to PLAY mode where you can interact with widgets. You can always get back to EDIT mode by pressing STOP

> Screenshot

Press Button to turn the LED On and Off

> Screenshot

Always feel free to experiment more! For example, attach an LED to [PWM](http://www.arduino.cc/en/Tutorial/Fading) Pin on your Arduino. Set the Slider Widget to control brightness of an LED. Just use the same steps described above.

**Happy Blynking!**
___

#Blynk on Raspberry Pi and Spark Core
Specific steps for Raspberry Pi
Specific steps for Spark Core 

#List Of Supported Hardware
List of devices goes here

#Blynk Commands
All the commands you can use in code
VirtualWrite

#Widgets
Always feel free to experiment more!

#Adding Support for your Hardware 
Always feel free to experiment more!



### Quickstart: Arduino + Ethernet shield

* Download the Blynk app ([App Store](https://itunes.apple.com/us/app/blynk-control-arduino-raspberry/id808760481?ls=1&mt=8), [Google Play](https://play.google.com/store/apps/details?id=cc.blynk)) 
* Get the Auth Token from the app
* Import this library to Arduino IDE. Guide [here](http://arduino.cc/en/guide/libraries)
* In Arduino IDE, select File -> Examples -> Blynk -> BoardsAndShields -> Arduino_Ethernet
* Update Auth Token in the sketch and upload it to Arduino
* Connect your Arduino with Ethernet shield to the internet

### Supported boards, WiFi, Serial, USB...

[See examples](examples/BoardsAndShields) with different connection types.

Full list of supported hardware is [here](http://community.blynk.cc/t/hardware-supported-by-blynk).

### Docs

* [Basics](./docs/Basics.md)
* [Widgets](./docs/Widgets.md)
* [Security](./docs/Security.md)
* [Platforms/Connection types](./docs/Platforms.md)
* [Troubleshooting](./docs/Troubleshooting.md)
* [Implementing your own library](./docs/Implementing.md)

### License

This project is released under The MIT License (MIT)


#Links

* [Kickstarter campaign](https://www.kickstarter.com/projects/167134865/blynk-build-an-app-for-your-arduino-project-in-5-m/description)
* [Blynk downloads, docs, tutorials](http://www.blynk.cc)
* [Blynk community](http://community.blynk.cc)
* [Facebook](http://www.fb.com/blynkapp)
* [Twitter](http://twitter.com/blynk_app)
