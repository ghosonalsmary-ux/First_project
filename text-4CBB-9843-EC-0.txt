‏tries = 0
‏while tries < 3:
‏    password = input("Enter password: ")
‏    has_capital = False
‏    has_small = False
‏    has_number = False
‏    has_symbol = False
‏    for char in password:
‏        if char.isupper():
‏            has_capital = True
‏        elif char.islower():
‏            has_small = True
‏        elif char.isdigit():
‏            has_number = True
‏        else:
‏            has_symbol = True
‏    if (len(password) >= 8 and has_capital and has_small and has_number and has_symbol):
‏        print("Strong Password")
‏        break
‏    else:
‏        print("Weak Password, you need:")
‏        if len(password) < 8:
‏            print("- 8 characters")
‏        if not has_capital:
‏            print("- capital letter")
‏        if not has_small:
‏            print("- small letter")
‏        if not has_number:
‏            print("- number")
‏        if not has_symbol:
‏            print("- symbol")
‏        tries += 1
‏        if tries == 3:
‏            print("Too many tries, try later")
