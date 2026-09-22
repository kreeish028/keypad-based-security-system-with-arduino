#  **Keypad-Based Security System with Arduino**

##  **Project Overview**

The **Keypad-Based Security System with Arduino** is a simple electronic security project designed to provide controlled access using a password. The system uses a **4×4 keypad** to enter a password and an **Arduino** to verify the entered password. Access is granted only when the correct password is entered.

This project demonstrates the basic concepts of **password authentication, digital input, Arduino programming, and security automation**.

## **Objectives**

* To develop a simple password-based security system.  
* To provide controlled access using a keypad.  
* To verify the entered password using Arduino.  
* To improve basic security through electronic authentication.  
* To understand keypad interfacing with Arduino.  
* To demonstrate automation using a microcontroller

##  

## **Working Principle**

## The **Keypad-Based Security System** works by accepting a password through the keypad and using Arduino to verify it. When the correct password is entered, Arduino activates the servo motor or electronic lock and grants access. If an incorrect password is entered, access is denied and the buzzer can give an alert. The LCD displays the system status such as **“Enter Password,” “Access Granted,”** or **“Access Denied.”**

## **Program**

\#include \<Wire.h\>  
\#include \<LiquidCrystal\_I2C.h\>  
\#include \<Keypad.h\>

// I2C LCD address  
LiquidCrystal\_I2C lcd(0x27, 16, 2);

// 4x4 Keypad  
const byte ROWS \= 4;  
const byte COLS \= 4;

char keys\[ROWS\]\[COLS\] \= {  
  {'1','2','3','A'},  
  {'4','5','6','B'},  
  {'7','8','9','C'},  
  {'\*','0','\#','D'}  
};

byte rowPins\[ROWS\] \= {9, 8, 7, 6};  
byte colPins\[COLS\] \= {5, 4, 3, 2};

Keypad keypad \= Keypad(  
  makeKeymap(keys),  
  rowPins,  
  colPins,  
  ROWS,  
  COLS  
);

void setup() {  
  lcd.init();  
  lcd.backlight();

  lcd

##  **Key Concept**

**Enter Password → Verify Password → Grant or Deny Access**

##  **Conclusion**

The **Keypad-Based Security System with Arduino** provides a simple and effective way to understand electronic access control. It combines a keypad, Arduino, display, buzzer, and locking mechanism to create a basic password-protected security system. The project can also serve as a foundation for developing advanced smart security systems.

## Result
<img width="1600" height="900" alt="RESULT" src="https://github.com/user-attachments/assets/347769b2-3185-4e70-9344-93cf52ccfa2a" />


