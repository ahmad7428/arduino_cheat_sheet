## Arduino Cheat Sheet
##### github.com/ahmad7428

## Comments
```
// This is a single line comment

/*
This is a
block comment
*/
```
## Variables
```
int any_variable = 58;
```
## Data types
```
byte a;		// 8 bit value without decimals
int a;		// 16 bit value without decimals
long a;		// 32 bit value without decimals
float a;	// 32 bit value with decimal points
```
## Arithematic in Arduino 
```
a = a + 2;	// Addition
b = b - 2;	// Subtraction
c = c * 2;	// Multiplication
d = d / 2;	// Division
```
## Comparison Operators
```
a == b 	  // a is equal to b
a != b 	  // a is not equal to b
a < b 	  // a is less than b
a > b 	  // a is greater than b
a <= b 	  // a is less than or equal to b
a >= b 	  // a is greater than or equal to b
```
## Logical Operations
```
x > 6 && x < 12   // AND operator
x > 6 || x < 12   // OR operator
!x > 6            // NOT operator
```
## Compound Assignments
```
x++       // increments by 1
x--       // decrmenets by 1
x += y 	  // increments x by +y
x -= y 	  // decrmenets x by -y
x *= y 	  // multiplies x by y
x /= y 	  // divides x by y
```
## Pin assignment
```
pin_1_name = 9;         // Assign a digital pin
pin_2_name = 3;
analog_pin_name = A0;   // Assign an analog pin
```
## Pin Operations
```
pinMode(pin_name, INPUT);                     // Sets pin as Input
pinMode(pin_name, OUTPUT);                    // Sets pin as Output

int any_variable_2 = digitalRead(pin_name);   // reads a digital (discrete) value at the specified pin and stores it in the variable
digitalWrite(pin_name, HIGH);                 // sets the mentioned pin voltage level HIGH
digitalWrite(pin_name, LOW);                  // sets the mentioned pin voltage level LOW

int any_variable = analogRead(pot);           // reads an analog value at the specified pin and stores it in the variable
analogWrite(any_variable);                    // improvises the read analog value onto the mentioned variable
```
## Structure
```
#include</*any Libraries you want to call*/>

pin_declaration = 9;    // Pin Declaration
int a = 8;              // Initialising and Declaring any variables

void setup(){
statements;
}

void loop(){
statements;
}
```
## Setup (Runs once at the start-up)
```
void setup(){
	pinMode(pin_name, OUTPUT);
}
```
## Loop (Keeps running until powered off)
```
void loop(){
	digitalWrite(pin_name, HIGH);
	delay(1000);
	digitalWrite(pin_name, LOW);
	delay(1000);
}
```
## Functions
```
int delayValue(){
	int v;
	v = analogRead(pot);
	v /= 4;
	return v;
}

// Calling a function
delayValue()
```
## Conditions
```
if (random_variable >= 55){
	digitalWrite(13, HIGH);
}
else if (random_variable <= 55){
	digitalWrite(13, LOW);
}
else{
	digitalRead(pin_name_2);
}
```
## Loops
```
// For Loop
for (int i = 0; i >= 50; i++){
	// This code inside for loop will be run 50 times
	digitalWrite(13, HIGH); // Turns Built-in LED ON
	delay(500);				// for 0.5 seconds
	digitalWrite(13, LOW);  // Turns Built-in LED OFF
	delay(500);				// for 0.5 seconds
}

// While Loop
while (pin_name_2 == 1){
	digitalWrite(13, HIGH);
}

// Do While Loop
do{
	digitalWrite(13, HIGH);
} while (pot <= 500);
```
## Arrays
```
int my_Array[] = {0,1,2,3,4,5,6,7,8,9}
my_Array[2] = 23; // declares value of the third element to 23
x = my_Array[5] // using a value from array. x is now equal to 6
```
## Opening a Serial Port on Arduino
```
void setup(){
	Serial.begin(9600);
}

void loop(){
	Serial.println(/* Anything you want to be sent to the Serial Monitor */);
}
```
