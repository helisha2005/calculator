# calculator
def calculator():
    while True:
        print("\n----- Calculator -----")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")
        
        try:
            choice = int(input("Enter your choice (1/2/3/4/5): "))
            
            if choice == 5:
                print("Exiting the calculator. Goodbye!")
                break
            elif choice in [1, 2, 3, 4]:
               
                num1 = float(input("Enter the first number: "))
                num2 = float(input("Enter the second number: "))
                
                # Perform calculation based on choice
                if choice == 1:
                    result = num1 + num2
                    print(f"{num1} + {num2} = {result}")
                elif choice == 2:
                    result = num1 - num2
                    print(f"{num1} - {num2} = {result}")
                elif choice == 3:
                    result = num1 * num2
                    print(f"{num1} * {num2} = {result}")
                elif choice == 4:
                    if num2 != 0:
                        result = num1 / num2
                        print(f"{num1} / {num2} = {result}")
                    else:
                        print("Error! Division by zero.")
            else:
                print("Invalid choice! Please choose a valid operation.")
                
        except ValueError:
            print("Invalid input. Please enter a number.")
            
calculator()

