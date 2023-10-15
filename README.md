# JavaSE-Variables

## 1. Variables declaration

In Java, you declare variables to store and manipulate data. 

In these examples:

- int, short, long, float, double, char, and boolean are primitive data types.

- String is a class for representing strings.

- Arrays allow you to store multiple values of the same type in a single variable.

- Objects are instances of classes and are created using the new keyword.

- Constants are declared using the final keyword and are typically written in uppercase.

When declaring a variable, you specify its type, followed by the variable name, an equal sign (=), and the initial value. The initial value is optional, and you can declare a variable without assigning a value if you plan to assign it later.

### 1.1. Primitive Data Types

```java
// Integer types
int age = 25;
short numberOfCars = 2;
long totalPopulation = 1500000000L; // Use 'L' for long literals

// Floating-point types
float temperature = 98.6f; // Use 'f' for float literals
double distance = 1500.75;

// Character type
char grade = 'A';

// Boolean type
boolean isJavaFun = true;
```

### 1.2. Reference Data Types

```java
// Strings
String message = "Hello, World!";

// Arrays
int[] numbers = {1, 2, 3, 4, 5};
String[] names = {"Alice", "Bob", "Charlie"};

// Objects
MyClass myObject = new MyClass();
```

### 1.3. Constants (using final keyword)

```java
final double PI = 3.14159;
final int MAX_SIZE = 100;
```

## 2. Variable scope

In Java, variable scope refers to the region of the code where a variable can be accessed. 

There are mainly two types of variables in terms of scope: local variables and instance variables (attributes).

### 2.1. Local Variables
Local variables are declared within a method, constructor, or block of code.

They are only accessible within the block of code where they are declared.

Local variables must be explicitly initialized before use.

```java
public class MyClass {
    // Instance variable (attribute)
    private int globalVar; // Initialized to default value (0 for int)

    public void myMethod() {
        // Local variable
        int localVar = 10; // Initialized to default value (0 for int)

        // Accessing both local and instance variables
        System.out.println("Local Variable: " + localVar);
        System.out.println("Instance Variable: " + globalVar);
    }
}
```

### 2.2. Instance Variables (Attributes)

Instance variables (or attributes) are declared within a class but outside any method, constructor, or block.

They are part of the object's state and have default values if not explicitly initialized.

For example, numeric types are initialized to 0, objects to null, and booleans to false.

```java
public class MyClass {
    // Instance variables (attributes)
    private int age;      // Initialized to default value (0 for int)
    private String name;   // Initialized to default value (null for objects)

    public void setAge(int newAge) {
        age = newAge;
    }

    public void setName(String newName) {
        name = newName;
    }

    public void displayInfo() {
        // Accessing instance variables
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```
