# yum-yum-burger
Lab 4.5 – Programming Challenge 1 – Yum Yum Burger Joint  
Write the Flowchart and Python code for the following programming problem and the pseudocode below.   
Write a program that will calculate the cost of purchasing a meal.  This program will include decisions and loops.  
Details of the program are as follows:
•	Your menu items only include the following food with accompanied price: 
o	Yum Yum Burger = .99
o	Grease Yum Fries = .79
o	Soda Yum = 1.09
•	Allow the user of the program to purchase any quantity of these items on one order. 
•	Allow the user of the program to purchase one or more types of these items on one order.
•	After the order is placed, calculate total and add a 6% sales tax. 
•	Print to the screen a receipt showing the total purchase price.

#siliky
#4.6


print("Welcome to the Yum Yum Burger Joint")

yumBurger_price = 0.99
greaseFries_price = 0.79
soda_price = 1.09
keepgoing_end = "no"
end = "no"
food_total = 0

while keepgoing_end == "no":
    while end == "no":
        print("Enter 1 for Yum Yum Burger")
        print("Enter 2 for Grease Yum Fries")
        print("Enter 3 for Soda Yum")
        order = int(input("Enter now ->"))
        if order == 1 or order == 2 or order ==3:
            if order == 1:
                burger = int(input("Enter the number of burgers you want"))
                food_total += (burger * yumBurger_price)
            elif order == 2:
                fries = int(input("Enter the number of fries you want"))
                food_total += (fries * greaseFries_price)
            elif order == 3:
                soda = int(input("Enter the number of sodas you want"))
                food_total += (soda * soda_price)
            else:
                print("you need to type 1, 2, 3")
        keepgoing_end = input("Do you want to end your order? (yes/no): ")
        if keepgoing_end == "yes":
            total = food_total * 1.06
            print("The total price is $", total)
            end = input("Do you want to end your order? (yes/no): ")
            if end == "yes":
                break
            elif end == "no":
                food_total = 0
                continue
        elif keepgoing_end == "no":
            continue
        
