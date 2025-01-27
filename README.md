# Interface-
package pkginterface.calculater;
import java.util.Scanner;
 interface Calculator {
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
}
// Implement the interface in SimpleCalculator
class SimpleCalculator implements Calculator {
@Override
public double add(double a, double b) {
return a + b;
}
@Override
public double subtract(double a, double b) {
return a - b;
}
@Override
public double multiply(double a, double b) {
return a * b;
}
@Override
public double divide(double a, double b) {
if (b == 0) {
System.out.println("Error: Division by zero is not allowed!");
return Double.NaN; // Return &quot;Not a Number&quot; if division by zero
}
return a / b;
}
}

public class InterfaceCalculater {
    public static void main(String[] args) {
        
Scanner scanner = new Scanner(System.in);
Calculator calculator = new SimpleCalculator();
System.out.println("Welcome to the Simple Calculator!");
// Input two numbers
System.out.print("Enter the first number:");
double num1 = scanner.nextDouble();
System.out.print("Enter the second number:");
double num2 = scanner.nextDouble();
// Perform calculations

System.out.println("\nResults:");
System.out.println("Addition:"  + calculator.add(num1, num2));
System.out.println("Subtraction:" + calculator.subtract(num1, num2));
System.out.println("Multiplication: " + calculator.multiply(num1, num2));
System.out.println("Division:"+ calculator.divide(num1, num2));
scanner.close();
}
}


Output:
Welcome to the Simple Calculator!
Enter the first number:5
Enter the second number:10

Results:
Addition:15.0
Subtraction:-5.0
Multiplication: 50.0
Division:0.5
BUILD SUCCESSFUL (total time: 12 seconds)
