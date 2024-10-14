<=>
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Enter the first number:");
    int num1 = scanner.nextInt();

    System.out.println("Enter the second number:");
    int num2 = scanner.nextInt();

    System.out.println("Enter the third number:");
    int num3 = scanner.nextInt();

    int highest = Math.max(Math.max(num1, num2), num3);
    int middle = (num1 + num2 + num3) - highest - Math.min(Math.min(num1, num2), num3);
    int lowest = Math.min(Math.min(num1, num2), num3);

    System.out.println("The numbers in order from highest to lowest are:");
    System.out.println(highest);
    System.out.println(middle);
    System.out.println(lowest);
  }
}

Months to days
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Enter the year:");
    int year = scanner.nextInt();

    System.out.println("Enter the month (1-12):");
    int month = scanner.nextInt();

    int daysInMonth = getDaysInMonth(year, month);

    System.out.println("The month " + month + " in the year " + year + " has " + daysInMonth + " days.");
  }

  public static int getDaysInMonth(int year, int month) {
    if (month == 2) {
      if (isLeapYear(year)) {
        return 29;
      } else {
        return 28;
      }
    } else if (month == 4 || month == 6 || month == 9 || month == 11) {
      return 30;
    } else {
      return 31;
    }
  }

  public static boolean isLeapYear(int year) {
    return (year % 4 == 0 && year % 100 != 0) || year % 400 == 0;
  }
}

celsius to farenheit

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Enter 1 to convert Celsius to Fahrenheit, or 2 to convert Fahrenheit to Celsius:");
    int choice = scanner.nextInt();

    if (choice == 1) {
      System.out.println("Enter the temperature in Celsius:");
      double celsius = scanner.nextDouble();
      double fahrenheit = celsiusToFahrenheit(celsius);
      System.out.println(celsius + " degrees Celsius is equal to " + fahrenheit + " degrees Fahrenheit.");
    } else if (choice == 2) {
      System.out.println("Enter the temperature in Fahrenheit:");
      double fahrenheit = scanner.nextDouble();
      double celsius = fahrenheitToCelsius(fahrenheit);
      System.out.println(fahrenheit + " degrees Fahrenheit is equal to " + celsius + " degrees Celsius.");
    } else {
      System.out.println("Invalid choice. Please try again.");
    }
  }

  public static double celsiusToFahrenheit(double celsius) {
    return (celsius * 9/5) + 32;
  }

  public static double fahrenheitToCelsius(double fahrenheit) {
    return (fahrenheit - 32) * 5/9;
  }
}

triangles
check gmail or

public class Main {
  public static void main(String[] args) {
    int rows = 5; // number of rows in the triangle

    for (int i = 1; i <= rows; i++) {
      for (int j = 1; j <= i; j++) {
        System.out.print("* ");
      }
      System.out.println();
    }
  }
}

calcu

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Enter the first number:");
    double num1 = scanner.nextDouble();

    System.out.println("Enter the second number:");
    double num2 = scanner.nextDouble();

    System.out.println("Enter the operation (+, -, *, /):");
    char operation = scanner.next().charAt(0);

    double result = 0;

    switch (operation) {
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
          System.out.println("Error: Division by zero!");
          return;
        }
        break;
      default:
        System.out.println("Error: Invalid operation!");
        return;
    }

    System.out.println("Result: " + result);
  }
}
