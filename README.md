# calculator
#calculator using python
import math

def Simple_calculator():
    print("Welcome to the Simple Calculator")
    print("----------------------------------")
    print("Available operations:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Power (x^y)")
    print("6. Square root (sqrt)")
    print("7. Trigonometric Functions (sin, cos, tan)")
    print("8. Logarithm (log base 10)")
    print("9. Factorial (!)")
    print("10. Modulus (%)")
    print("11. Constants (pi, e)")
    print("12. Exit")
    print("It runs until you select exit")

    while True:
        choice = int(input("\nEnter the operation number (1-12): "))

        if choice == '1':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print(f"Result: {a + b}")

        elif choice == '2':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print(f"Result: {a - b}")

        elif choice == '3':
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            print(f"Result: {a * b}")

        elif choice == '4':
            a = float(input("Enter numerator: "))
            b = float(input("Enter denominator: "))
            if b != 0:
                print(f"Result: {a / b}")
            else:
                print("Error: Division by zero")

        elif choice == '5':
            a = float(input("Enter base: "))
            b = float(input("Enter exponent: "))
            print(f"Result: {math.pow(a, b)}")

        elif choice == '6':
            a = float(input("Enter a number to Square it : "))
            if a >= 0:
                print(f"Result: {math.sqrt(a)}")
            else:
                print("Error: Cannot take square root of negative number")

        elif choice == '7':
            angle = float(input("Enter angle in degrees: "))
            radians = math.radians(angle)
            print(f"sin({angle}) = {math.sin(radians)}")
            print(f"cos({angle}) = {math.cos(radians)}")
            print(f"tan({angle}) = {math.tan(radians)}")

        elif choice == '8':
            num = float(input("Enter number: "))
            if num > 0:
                print(f"log10({num}) = {math.log10(num)}")
            else:
                print("Error: Logarithm undefined for non-positive numbers")

        elif choice == '9':
            num = int(input("Enter a non-negative integer: "))
            if num >= 0:
                print(f"{num}! = {math.factorial(num)}")
            else:
                print("Error: Factorial of negative number is undefined")

        elif choice == '10':
            a = int(input("Enter first number: "))
            b = int(input("Enter second number: "))
            print(f"Result: {a % b}")

        elif choice == '11':
            print(f"Pi = {math.pi}")
            print(f"e  = {math.e}")

        elif choice == '12':
            print("Calculation Ended. Goodbye!")
            break

        else:
            print("Invalid choice. Please select from 1 to 12.")

# Run the calculator
Simple_calculator()

