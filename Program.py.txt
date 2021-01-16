''' Customer can withdraw cash from an Automatic Teller Machine(ATM).
     => WITHDRAW IS REFUSED IF AMOUNT ENTERED > CURRENT BALANCE
     => WITHDRAW IS REFUSED IF AMOUNT ENTERED > DAILY LIMIT
     => IF CURRENT BALANCE < 5000, THEN CHARGE OF 20% IS MADE
     => IF CURRENT BALANCE >=5000, NO CHANGE IS MADE
    Write a program which inputs a request for a sum of money, decides if a withdraw can be made and calcultes any charge.
    Appropriate output messages should be included.
'''
current=3000
daily=int(input("enter daily limit : "))
withdraw=int(input("enter withdraw : "))

if (withdraw>current and withdraw>daily):
    
    print("Error withdraw is refused")
    
else:
    if current<5000:
        balance=withdraw*0.02
        current=current-balance
        print(f"withdraw amount is {withdraw} And current balanc is {current}")
    else:
        print(f"withdraw amount is {withdraw} And current balanc is {current}")

