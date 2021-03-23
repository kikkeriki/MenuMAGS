import random

flag = 0
x = []

for i in range(1, 11):
    x.append(random.randint(1, 500))
print("--------------LIST--------------")
print(x)

#option 1
def sumofelements(x):
    print("-----------------------------")
    b = sum(x)                              # add all numbers in list
    print("Sum of all elements", b)         # print added value
    print("-----------------------------")

#option 2
def isPrime(i):
    for p in range(2, i - 1):
        if i % p == 0:
            flag = 1
            break
    else:
        flag = 0
        if flag == 0:
            print(i)

#option 3
def evenodd(x):
    evenlist = []                           #new even list
    oddlist = []                            #new odd list
    for i in x:
        if (i % 2 == 0):                    #if elements is divisble by 2
            evenlist.append(i)              #add to even list
    else:
        oddlist.append(i)                   #if not divisible by 2 add to odd list
        print("-----------------------------")
        print("Even lists:", evenlist)      #print even list
        print("Odd lists:", oddlist)        #print odd list
        print("-----------------------------")

#option 4
def smolarge(x):
    print("-----------------------------")
    print("Smallest number in the list is:", min(x))                           #prints minimum value in list
    print("largest number in the list is:", max(x))                            #prints maximum value in list
    print("Here is the numbers sorted from smallest to largest: ", sorted(x))  #sorts list from min to max
    print("-----------------------------")

#option 5
def removeprime():
    print("how")

#option6
def dups():
    remover = []                #new list
    for i in x:                 #check elements in list
        if i not in remover:    #checks elements in remover
            remover.append(i)   #adds unique elements to new list
    print("-----------------------------")
    print("The original list is : ", x)                     #print old list
    print("The list after removing duplicates : ", remover) #print new list
    print("-----------------------------")

#option 7
def freq():
    print("how")

loop = 1

while loop == 1:
    print()
    print("-----------------menu-----------------")
    print("1. Sum of all elements of a list")
    print("2. to check if a number in a list is prime")
    print("3. make two list - even numbers and odd numbers")
    print("4. show largest and smallest number")
    print("5. Remove prime and make a new list of prime numbers")
    print("6. remove duplicates (if any)")
    print("7. Frequency of each number")
    print("8. Exit")
    print(50*'-')

    option = int(input("Please Pick an option: "))
    print()

    if option == 1:
        sumofelements(x)
    elif option == 2:
        print(30 * '-')
        print(x)
        for i in x:
            (isPrime(i))
        print(30 * '-')
    elif option == 3:
        evenodd(x)
    elif option == 4:
        smolarge(x)
    elif option == 5:
        print("no")
    elif option == 6:
        dups()
    elif option == 7:
        freq()
    elif option == 8:
        print("Thanks for you for your time")
        loop = 0
    else:
        print("Invalid option please try again")
