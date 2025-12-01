# Resturent-Menu
#Making for the Resturent  to take the order and shows the amount to paying to onwer
<br>
# Take customer name
name = input("Enter the name of person: ")
print("Welcome to your restaurant,", name)

# Menu dictionary
menu = {
    "pizza": 200,
    "burger": 300,
    "salad": 400,
    "coffee": 500
}

# Display menu properly
print("Menu:")
for item, price in menu.items():
    print(f"{item}: {price}")

# Initialize total order
total_order = 0

# First order
item1 = input("Enter the item for order: ")
if item1 in menu:
    total_order += menu[item1]
    print(f"Your {item1} order is confirmed.")
else:
    print("Out of stock")

# Ask for another order
another_order = input("Do you want to add another item (yes/no)? ").lower()
if another_order == "yes":
    item2 = input("Enter the second item for order: ")
    if item2 in menu:
        total_order += menu[item2]
        print(f"Your {item2} order is confirmed.")
    else:
        print("Out of stock")

# Final bill
print("Your total amount is:", total_order)
print("Thank you!")




