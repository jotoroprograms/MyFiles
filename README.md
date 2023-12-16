import time
#creating functions----------------------------------------------------------------------------------------------------------------------------------------------------------------
def text():
    print('Press 1 to withdraw money')
    print('Press 2 to deposit money')
    print('Press 3 to see account balance')
    print('Press 4 to cancel transation')
    print('---------------------------------------')
def withdraw1(total,withdrawal):
    withdrawal=int(input('enter amount to withdraw:'))
    if withdrawal>sum(total):
        print('insufficient funds')
    else:
        sum(total)-withdrawal
        q=sum(total)-withdrawal
        print('succesfully withdrew',withdrawal,'Qr from you bank')
        print('---------------------------------------')
        print('account balance:',q)
    return 
def deposit2(total,deposit):
    deposit=int(input('enter amount to deposit:'))
    total.append(deposit)
    print('succesfully deposited',deposit,'Qr in your bank')
    print('---------------------------------------')
    print('account balance:',sum(total))
    return
def ATM(total):
    text()
    while True:
        r=int(input())
        if r==1:
            withdraw1(total,withdraw1)
            print('---------------------------------------')
            print('Do you want to continue transaction?')
            l=int(input('Press 1 for yes and 2 for no:'))
            if l==2:
                print('Thank you for using our ATM, come back again!')
                print('transaction ended on',
                       time.strftime('%H:%M:%S'),time.strftime('%p'))
                break;
            elif l==1:
                print('---------------------------------------')
                text()
            else:
                print('error')
        elif r==2:
            deposit2(total,deposit2)
            print('---------------------------------------')
            print('Do you want to continue transaction?')
            l=int(input('Press 1 for yes and 2 for no:'))
            if l==2:
                print('Thank you for using our ATM, come back again!')
                print('transaction ended on',
                        time.strftime('%H:%M:%S'),time.strftime('%p'))
                break;
            elif l==1:
                print('---------------------------------------')
                text()
            else:
                print('error')
        elif r==3:
            print(sum(total))
            print('---------------------------------------')
            print('Do you want to continue transaction?')
            l=int(input('Press 1 for yes and 2 for no:'))
            if l==2:
                print('Thank you for using our ATM, come back again!')
                print('transaction ended on',
                        time.strftime('%H:%M:%S'),time.strftime('%p'))
                break;
            elif l==1:
                print('---------------------------------------')
                text()
            else:
                print('error')

        elif r==4:
            print('Are you sure you want to end transaction?')
            l=int(input('Press 1 for yes and 2 for no:'))
            if l==1:
                print('Thank you for using our ATM, come back again!')
                print('transaction ended on',
                        time.strftime('%H:%M:%S'),time.strftime('%p'))
                break;
            elif l==2:
                print('---------------------------------------')
                text()
            else:
                print('error')

        else:
            print('error')
#creating lists----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Nelson=[]
Muamar=[]
Frank=[]
Luna=[]
Alexei=[]
#main program-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
while True:
    z=int(input('enter account PIN:'))
    while z!=1489 and z!=2256 and z!=8849 and z!=6285 and z!=3627:
         print("This account doesn't exist")
         z=int(input('enter account PIN:'))
    if z==1489:
          print('---------------------------------------')
          print('Welcome Nelson')
          print('---------------------------------------')
          ATM(Nelson)
    elif z==2256:
          print('---------------------------------------')
          print('Welcome Muamar')
          print('---------------------------------------')
          ATM(Muamar)
    elif z==8849:
          print('---------------------------------------')
          print('Welcome Frank')
          print('---------------------------------------')
          ATM(Frank)
    elif z==6285:
          print('---------------------------------------')
          print('Welcome Alexei')
          print('---------------------------------------')
          ATM(Alexei)
    else:
          print('---------------------------------------')
          print('Welcome Luna')
          print('---------------------------------------')
          ATM(Luna)
        

