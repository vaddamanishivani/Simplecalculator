# Simplecalculator
import java.util.Scanner;

public class SimpleCalculator . java {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Simple Calculator");
        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();

        System.out.print("Enter an operator (+, -, *, /): ");
        String input = scanner.next();
        char operator;

        // Validate operator input
        if (input.length() != 1) {
            System.out.println("Error! Invalid operator.");
            return;
        }
        operator = input.charAt(0);

        double result;

        switch (operator) {
            case '+':
                result = num1 + num2;
                break;

            case '-':
                result = num1 - num2;
                break;

            case '*':
                result = num1 * num2;
                break;

            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error! Division by zero.");
                    return;
                }
                break;

            default:
                System.out.println("Error! Invalid operator.");
                return;
        }

        System.out.println("The result is: " + result);
    }
}
