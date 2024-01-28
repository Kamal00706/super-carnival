#Personal Expense Tracker

Starting_balance = float(input("Enter your starting balance:"))

def add_expense(name, cost, balance):
    # Subtract the cost from the balance and return the new balance
    new_balance = balance - cost
    return new_balance, f"{name}: ${cost}"

# Use a loop to keep asking for expenses
expenses = []
while True:
    user_input = input("Do you want to add an expense? (yes/no): ")
    if user_input.lower() == 'yes':
        expense_name = input("Enter the expense name: ")
        expense_cost = float(input("Enter the expense cost: $"))
        starting_balance, expense_record = add_expense(expense_name, expense_cost, starting_balance)
        expenses.append(expense_record)
    elif user_input.lower() == 'no':
        break
    else:
        print("Please enter 'yes' or 'no'.")


print("Here are all your expenses:")
for expense in expenses:
    print(expense)
print(f"Your final balance is: ${starting_balance}")


