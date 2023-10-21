def calculate(num1, num2, act):
    if(act=='+'):
        total=num1+num2
    elif(act=='-'):
        total=num1-num2
    elif(act=='*'):
        total=num1*num2
    elif(act=='/'):
        total=num1/num2
    else:
        print("input not recognized")
    return total

def calc2():
    user_input=input("Enter a num1 act num2 (with a space between them): ")   #Gets the values
    var1, action, var2=user_input.split()     #assigns the values into the variables
    if(action=='/' and var2==0):      #checks for division by 0
        print("YOU CAN'T DIVIDE BY ZERO!!!")
    else:
        print(calculate(float(var1), float(var2), action))     #calls the 'calculating' function, recives and prints the total of act

def calc3():
    user_input=input("Enter a num1 act1 num2 act2 num3 (with a space between them): ")      #Gets the values
    var1, action1, var2, action2, var3=user_input.split()           #assigns the values into the variables
    if(action1=='/' and var2==0 or action2=='/' and var3==0):      #checks for division by 0
        print("YOU CAN'T DIVIDE BY ZERO!!!")
    elif((action2=='*' or action2=='/') and (action1=='+' or action2=='-')):    #checks if act2 should be done before act1 (order of operation)
        total=calculate(float(var2), float(var3), action2)     #calls the 'calculating' function, recives the total of act2
        print(calculate(float(var1), float(total), action1))     #calls the 'calculating' function, assigns the total of act2 as num2, recives and prints the total of act1
    else:                                                             #act1 is done before act2 (order of operation)
        total=calculate(float(var1), float(var2), action1)         #calls the 'calculating' function, recives the total of act1
        print(calculate(float(total), float(var3), action2))     #calls the 'calculating' function, assigns the total of act1 as num1, recives and prints the total of act2

def main():
    amount=float(input("How many numbers? (2-3 numbers) "))
    if(amount==2):
        calc2()
    elif(amount==3):
        calc3()
    else:
        print("I SAID TWO OR THREE NUMBERS")

main()           #starts program
