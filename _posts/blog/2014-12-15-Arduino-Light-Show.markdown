---
layout: post
title: "Making Christmas Lights with the Arduino"
date: 2014-12-15 23:46:00
author: Erik Xu
categories: 
- blog
- Guides
img: post04.jpg # (850x450)
thumb: thumb04.png # (70x70)
---

### Christmas season is coming! Make your own Christmas lights at home with an Arduino and LEDs for energy efficiency and minimal cost!

An [Arduino](http://arduino.cc/) is an inexpensive and portable microcontroller. Microcontrollers are hardware that interacts with the environment through the use of sensors, LEDs, and other hardware components. What makes it special is that it is widely available and well-known to most electronics hobbyist. There are a lot of community-based support and documentation for the Arduino. As a result, it is simple for anyone to get it running in no time.
<!--more-->
Let's get started, shall we?

The hardware needed are:
<br><b>1.</b> Arduino (Available on [Adafruit](http://www.adafruit.com/products/50) and [SparkFun](https://www.sparkfun.com/products/11021))<br>
<b>2.</b> Breadboard ([Amazon.com](http://www.amazon.com/s/ref=nb_sb_noss_1?url=search-alias%3Daps&field-keywords=breadboard))<br>
<b>3.</b> LEDs ([eBay.com](http://www.ebay.com/sch/i.html?_odkw=cheap+light+emitting+diode&_from=R40%7CR40&_osacat=0&_from=R40&_trksid=p2045573.m570.l1313.TR4.TRC2.A0.H0.Xlight+emitting+diode&_nkw=light+emitting+diode&_sacat=0))<br>
<b>4.</b> Resistors ([eBay.com](http://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR11.TRC1.A0.H0.Xresistors&_nkw=resistors&_sacat=0), resistors are needed so the LEDs don't short themselves out from the high voltage) 

After purchasing all the material, we can now start our Christmas lights assembly.
First of all, begin by downloading the [Arduino IDE](http://arduino.cc/en/main/software) (Integrated Development Environment) which is where we will type our code to the Arduino to control the LEDs.

Connect your Arduino cable to your computer's USB port.
Your computer should automatically recognize the initially unknown device.
Run the downloaded IDE and go to the Tools menu on the top. Head down to <b>Serial Port</b> and choose <i>/dev/tty.usbmodem1451</i>. This is the communication serial which your computer will be interacting with the Arduino.

Now, we want to setup our miniature Christmas lights circuit.
<br><b>Step 1</b>
Connect two resistors to two separate rows on the breadboard.
<img class="blogpost" src="{{ "/assets/img/blog/resume-tips/1.png" | prepend: site.baseurl }}" alt="">
<br>

<b>Step 2</b>
Connect the longer metal leg of each LED to the other end of the resistors.
<img class="blogpost" src="{{ "/assets/img/blog/resume-tips/1.png" | prepend: site.baseurl }}" alt="">
<br>

<b>Step 3</b>
Connect 2 jumper cables to pins 12 and 13 on your Arduino and connect the other end to the leg of the resistors that are not connected to the LEDs.
<img class="blogpost" src="{{ "/assets/img/blog/resume-tips/1.png" | prepend: site.baseurl }}" alt="">
<br>

<b>Step 4</b>
Finally, connect a wire to ground and to the other end of the LEDs.
<img class="blogpost" src="{{ "/assets/img/blog/resume-tips/1.png" | prepend: site.baseurl }}" alt="">
This is what it should look like at the end after everything has been connected!
<br>

<blockquote>
1. int led = 13;<br>
2. int led1 = 12;<br>
3.
4. void setup() {<br>                
5. // initialize the digital pin as an output.<br>
6.  pinMode(led, OUTPUT);     <br>
7.  pinMode(led1, OUTPUT);   <br>
8. }<br>
9.
10. void loop() {<br>
11.   digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)<br>
12.	  digitalWrite(led1, LOW);<br>
13.	  delay(1000);               // wait for a second<br>
14.	  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW<br>
15.	  digitalWrite(led1, HIGH);<br>
16.	  delay(1000);               // wait for a second<br>
17. }
</blockquote>

With this, I leave you to create your own array and entire tree of Christmas lights!
Check out other cool Arduino projects on [Instructables](http://www.instructables.com/id/Arduino-Projects/) and other various websites.