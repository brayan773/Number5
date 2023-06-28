Import java.util.Scanner;

Public class Calculator {
    Public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print(“Enter the first number: “);
        Double num1 = scanner.nextDouble();

        System.out.print(“Enter an operator (+, -, *, /): “);
        Char operator = scanner.next().charAt(0);

        System.out.print(“Enter the second number: “);
        Double num2 = scanner.nextDouble();

        Double result = calculate(num1, operator, num2);
        System.out.println(“Result: “ + result);

        Scanner.close();
    }

    // Method to perform the calculation based on the operator
    Public static double calculate(double num1, char operator, double num2) {
        Double result = 0;

        Switch (operator) {
            Case ‘+’:
                Result = add(num1, num2);
                Break;
            Case ‘-‘:
                Result = subtract(num1, num2);
                Break;
            Case ‘*’:
                Result = multiply(num1, num2);
                Break;
            Case ‘/’:
                Result = divide(num1, num2);
                Break;
            Default:
                System.out.println(“Invalid operator!”);
        }

        Return result;
    }

    // Method to perform addition
    Public static double add(double num1, double num2) {
        Return num1 + num2;
    }

    // Method to perform subtraction
    Public static double subtract(double num1, double num2) {
        Return num1 – num2;
    }

    // Method to perform multiplication
    Public static double multiply(double num1, double num2) {
        Return num1 * num2;
    }

    // Method to perform division
    Public static double divide(double num1, double num2) {
        If (num2 == 0) {
            System.out.println(“Error: Cannot divide by zero!”);
            Return 0;
        }
        Return num1 / num2;
    }
}
