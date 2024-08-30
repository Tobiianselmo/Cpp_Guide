
# Introduction to Classes in C++

In C++, a **class** is a structure that allows you to define a custom data type, which can include both data and functions. Classes are a way to organize and structure code, allowing you to group related attributes (variables) and methods (functions).

## Simple Explanation

Think of a class as a template or mold for creating objects. An object is an instance of that class. For example, if you have a class called `Car`, each specific car you create using that class will be a different object, but all will share the characteristics and behaviors defined in the `Car` class.

## Contents of a Class

A class in C++ generally has the following components:

1. **Class Name**: It is the identifier you give to the class. For example: `class Car { ... };`.

2. **Attributes (member variables)**: These are the variables that belong to the class and represent the properties or characteristics of the objects created from the class.
   - Example: `int speed;`, `string color;`.

3. **Methods (member functions)**: These are the functions that belong to the class and define the behaviors of the objects created from the class.
   - Example: `void accelerate();`, `void brake();`.

4. **Constructors**: These are special functions that are automatically called when an object of the class is created. They are used to initialize the attributes.
   - Example: `Car(string c, int s) { color = c; speed = s; }`.

5. **Destructors**: These are special functions that are called when an object of the class is destroyed (e.g., when it goes out of scope). They are used to clean up resources if necessary.
   - Example: `~Car() { // release resources }`.

6. **Access Modifiers**: These are keywords that determine who can access the members of the class. The main ones are:
   - `public`: Members are accessible from outside the class.
   - `private`: Members are only accessible from within the class.
   - `protected`: Members are accessible from the class and derived classes (inheritance).

## Example of a Class in C++

```cpp
#include <iostream>
using namespace std;

class Car {
private:
    int speed;
    string color;

public:
    // Constructor
    Car(string c, int s) {
        color = c;
        speed = s;
    }

    // Method to accelerate
    void accelerate() {
        speed += 10;
    }

    // Method to display details
    void displayDetails() {
        cout << "Color: " << color << ", Speed: " << speed << " km/h" << endl;
    }
};

int main() {
    // Create an object of the Car class
    Car myCar("Red", 50);

    // Use methods of the object
    myCar.accelerate();
    myCar.displayDetails();

    return 0;
}
```

In this example, `Car` is a class with two attributes (`speed` and `color`) and two methods (`accelerate` and `displayDetails`). The constructor is used to initialize a `myCar` object with a color and an initial speed. Then, you can call the methods to manipulate the object.

This structure allows you to model real-world concepts in your program, making the code more organized and reusable.
