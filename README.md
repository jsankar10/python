loop=True
while loop:
    password = input("password:")
    if password =="daamu":
        print("welcome to pycharm")

        print("(what can i do for you)")
        print("1.Multiplication calculator")
        print("2.To find armstrong numbers")
        print("3.To find string")
        find=int(input("Enter your choice:"))
        if find==1:
            print("mathematical calculator")
            a = int(input("Enter 1st no.:"))
            b = int(input("Enter 2nd number:"))
            print("1.add")
            print("2.sub")
            print("3.mul")
            print("4.div")
            choose = int(input("entre ur choise:"))

            match choose:
                case 1:
                    print("sum =", a + b)
                case 2:
                    print("sub =", a - b)
                case 3:
                    print("mul=", a * b)
                case 4:
                    print("division =", a / b)
            if input("Do you want to continue (y/n):") !='y':
                break
        if find==2:
            while True:
                num = int(input("enter a number"))
                sum = 0
                temp = num
                while temp > 0:
                    digit = temp % 10
                    sum += digit ** 3
                    temp //= 10
                if num == sum:
                    print("it is an armstrong")
                else:
                    print("it is not an armstrong")
                if input("Do you want to continue (y/n):") != 'y':
                    break
        if find==3:
            while True:
                str = input("Enter a string:")
                print("1.string length")
                print("2.Upper to lower")
                print("3.Lower to upper")
                print("4.Replace string with others")
                print("5.Replace char with others")
                choise = int(input("Enter your choice:"))
                match choise:
                    case 1:
                        print(len(str))
                    case 2:
                        print(str.lower())
                    case 3:
                        print(str.upper())
                    case 4:
                        str1 = input("Enter new string")
                        print(str.replace(str, str1))
                    case 5:
                        str1 = input("in" + str + ",What character you want to change:")
                        str2 = input("What character you want to replace:")
                        result = ""
                        for i in range(len(str)):
                            if (str[i] == str1):
                                result = result + str2
                            else:
                                result = result + str[i]
                        print("\nModified string:", result)

                if input("do you want to continue (y/n)") != 'y':
                    break
        break
    else:
        print("incorrect password")
        loop==False
