# What Is the Entry Point of a Java Program?
In Java, the program begins execution from the main() method. It's the entry point the Java Virtual Machine (JVM) looks for to start running your code.

If the JVM doesn't find a main() method with the proper signature, it won't execute the program. When execution starts, a special thread known as a daemon thread is created and remains active until the Java program ends.

# Example of a Valid main() Method Signature

    public static void main(String[ ] args)

## Explanation of Components:

### public: 
An access modifier allowing the JVM (from outside your class) to access this method.

### static: 
Allows the JVM to run the method without creating an object of the class.

### void: 
Indicates the method doesn't return any value.

### main: 
The method's name—recognized by the JVM as the program's starting point.

### (String[ ] args): 
A parameter that can accept command-line arguments as an array of Strings.

# Why Is the main() Method Public?
The main() method is declared as public so that it can be accessed from outside the class—specifically by the JVM, which is not part of your class code.

# Why Is the main() Method Static?
The static keyword means that the method belongs to the class, not an instance. This is necessary because the JVM needs to call this method without first creating an object of your class.

It helps save memory and ensures the program can launch directly.

# Why Is the Return Type of main() Void?
Since the program doesn't need to return anything to the JVM, void is used. Even though you can technically use a return statement, it wouldn't return a value; it just ends the method's execution.

Once the main() method completes, the program terminates, so returning a value is pointless.

# What Is main?
main is simply the method name that the JVM looks for when beginning program execution. It’s not a Java keyword—just a special identifier the JVM expects.

# Can a Java Program Run Without a main() Method?
Yes, in versions before Java 8, it was possible to execute code without a main() method by using a static block. Static blocks are executed when the class is loaded into memory.

However, in Java 8 and above, this approach no longer works.

#### Example:
    class JavaPlusDSA {
        static {
            System.out.println("Executed without main method!");
        }
    }
# What Are Comments in Java?
Comments are used to explain code, improve readability, or temporarily disable parts of code for testing.

## Types of Comments:
Single-line comment: Begins with //

## Multi-line comment: 
Starts with /* and ends with */
