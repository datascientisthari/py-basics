# py-basics
my career starting programming
print('welcome to harry\'s world bank ATM')
restart = ('Y')
chances = 3
balance = 230.12
while chances >= 0:
    pin = int(input('please enter your 4 digit pin'))
    if pin == (2345):
        print('you entered your pin correctly\n')
        while restart not in ('n','N','NO','no'):
            print('please press 1 for your balance\n')
            print('please press 2 to make a withdrawl\n')
            print('please press 3 to pay in\n')
            print('please press 4 to return card\n')
            option = int(input('what would you like to choose?'))
            if option == 1:
                print('your balance is A£',balance,'\n')
                restart = input('would you like to go back? ')
                if restart in ('n','N','no','No'):
                    print('thank you')
                    break
            elif option == 2:
                option2 = ('y')
                withdrawl = float(input('how much would you like to withdraw ? \nA£10/A£20/A£40/A£60/A£80/A£100'))
                if withdrawl in [10,20,40,60,80,100]:
                    balance = balance - withdrawl
                    print('\nyour balance is now A£',balance)
                    restart =  input('would you like to go back?')
                    if restart in ('n','N','No','no'):
                        print('thank you')
                        break
                elif withdrawl != [10,20,40,60,80,100]:
                    print('invalid amount ,please re-try\n')
                    restart = ('y')
                elif withdrawl == 1 :
                    withdrawl = float(input('please enter desired amount: '))

            elif option ==3 :
                pay_in = float(input('how much would you like to pay in?'))
                balance = balance + pay_in
                print('\nyour balance is now A£',balance )
                restart = input('would you like to go back ? ')
                if restart in ('n','N','No','no'):
                    print('thank you')
                    break
            elif option == 4:
                    print('please wait whilst syour card is returned...\n')
                    print('thank you for your service')
                    break
            else:
                    print('please enter  a correct number.\n')
                    restart = ('y')
    elif pin != ('2345'):
        print('incorrect password')
        chances = chances - 1
        if chances == 0:
            print('\nNo more tries')
            break
