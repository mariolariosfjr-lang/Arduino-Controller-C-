# <ArduinoCPP/arduinoController.h>
This is a arduino controller for c++
# Compile
```css
g++ main.cpp ~/ArduinoCPP-lib/arduinoController.cpp -I~/ArduinoCPP-lib -o main
./main
```
# Who compiled:
I used headers (.h) (.hpp)
My name is Mario
Here
# arduinoController.h
```h
#ifndef ARDUINOCONTROLLER_H
#define ARDUINOCONTROLLER_H

#include <chrono>
#include <thread>
#include <iostream>

// Delay function (like Arduino)
void delayTheArduino(unsigned long milliseconds);

// Free functions outside any class
void control();
void repeat();

#endif
```
# arduinoController.cpp
```cpp
#include "arduinoController.h"

void delayTheArduino(unsigned long milliseconds) {
    std::this_thread::sleep_for(std::chrono::milliseconds(milliseconds));
}

void control() {
    std::cout << "Controlling Arduino..." << std::endl;
    delayTheArduino(9600);
}

void repeat() {
    std::cout << "Repeating Arduino actions..." << std::endl;
}
```
# main.cpp(test)
```cpp
#include <ArduinoCPP/arduinoController.h>

int main() {
    control();
    repeat();
    return 0;
}
```



