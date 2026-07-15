# Cool-Calculator
Cool calculator, Is a custom calculator that I am designing. 

#June 10
Thought it would be a fun project to build a custom calculator from scratch.

#June 11
Time Spent: 30 minuteds
I ordered the parts I would need from ali express

#June 30
Time Spent 2 hours
A handful of components arrived, so I started modeling my case using my new calipers (much better than my old measuring tape. Lol)

#July 1
Time Spent: 2 Hours
first iteration of the case finished (printed overnight)
Couple mistakes. Modeled up a second iteration and printed it. This one worked but was super ugly.

#July 2
Time Spent: 1 1/2 hours
Modeled and printed a new, case that both looked good, and all the parts fit perfectly. Also printed it in some new black filament (arrived today jayo 4.4kg for 50 bucks on amazon) instead of the ugly multi color stuff I was using before
<img width="2020" height="1360" alt="image" src="https://github.com/user-attachments/assets/c6a8287d-aa03-4d6b-8f42-1d235d70a4bd" />

#July 10
Time Spent: 2 hours
Troubleshooting ESP32
ESP would no take code from arduino IDE. Spent hours trying everything. eventually discovered corrupted library and fixed it. Finally worked. Came back later and hooked up my LCD screen, couldn't get the text to appear for a long time until I learned that you had to tune the screen by spinning a screw on the back

Progress:
Modeled and printed a case, Hooked up LCD screen and currently wiring 4x4 matrix keypad.


<img width="4032" height="3024" alt="image" src="https://github.com/user-attachments/assets/354603b7-1038-40b1-8327-1673736c15d3" />


BOM:
ESP32 Ali express 8 bucks - already ordered with own money
4x4 matrix keyboard Ali express 5 bucks - already ordered with own money
lcd screen ali express 6 bucks - already ordered with own money
Jayo 4.4kg filament 50 bucks - already ordered with own money


Code: (not final)

#include <Wire.h>
#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);

void setup() {
  Wire.begin(21, 22);

  lcd.init();
  lcd.backlight();

  lcd.setCursor(0, 0);
  lcd.print("Hello World!");

}

void loop() {
}
 
