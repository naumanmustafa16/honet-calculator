# honet-calculator
hyperskills-honest calculator

# write your code here
M = 0

while True:
    msg = ''
    msg_6 = " ... lazy"
    msg_7 = " ... very lazy"
    msg_8 = " ... very, very lazy"
    msg_9 = "You are"
    msg_96 = msg_9 + msg_6
    msg_96_7 = msg_96 + msg_7
    msg_96_7_8 = msg_96_7 + msg_8
    message0 = 'Enter an equation'
    print(message0)

    x, oper, y = input().split()
    # print(M)
    if x == 'M':
        x = M
    if y == 'M':
        y = M
    def is_one_digit(v):
        if float(v) > -10 and float(v) < 10 and float(v).is_integer():
            return True
        else:
            return False

    # print(is_one_digit(float(x)))
    # print(is_one_digit(float(y)))

    if is_one_digit(x) and is_one_digit(y) == True:
        msg = msg + msg_6


    if (float(x) == 1 or float(y) == 1) and (oper == '*') == True:
        msg = msg + msg_7

    if (float(x) == 0 or float(y) == 0) and (oper == '*' or oper == '+' or oper == '-') == True:
        msg = msg + msg_8

    if msg != "":
        msg = msg_9 + msg
        print(msg)






    def isflotrdig(num):
        try:
            float(num)
            return True
        except ValueError:
            return False
    x_type = isflotrdig(x)
    y_type = isflotrdig(y)

    if ((x_type and y_type) and (oper in ['+','-','*','/'])) == 1:
        if oper == '+':
            # print(x)
            result = float(x) + float(y)
            print(result)
            # print(len(str(int(result))))
            # print(result % 1 == 0)
            store = input('Do you want to store the result? (y / n):')
            if (store == 'y' and result % 1 == 0 and len(str(int(result))) == 1) == True:
                store_1 = input("Are you sure? It is only one digit! (y / n)")
                if store_1 == 'y':
                    store_2 = input("Don't be silly! It's just one number! Add to the memory? (y / n)")
                    if store_2 == 'y':
                        store_3 = input("Last chance! Do you really want to embarrass yourself? (y / n)")
                        if store_3 == 'y':
                            M = result
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                        elif store_3 == 'n':
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                    elif store_2 == 'n':
                        choose = input('Do you want to continue calculations? (y / n):')
                        if choose == 'y':
                            continue
                        elif choose == 'n':
                            break
                elif store_1 == 'n':
                    choose = input('Do you want to continue calculations? (y / n):')
                    if choose == 'y':

                        continue
                    elif choose == 'n':
                        break
            elif store == 'y' and (result % 1 != 0 or (len(str(int(result))) > 1)) == True:
                M = result
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break
            elif store == 'n':
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break

        elif oper == '-':
            result = float(x) - float(y)
            print(result)
            store = input('Do you want to store the result? (y / n):')

            if (store == 'y' and result % 1 == 0 and len(str(int(result))) == 1) == True:
                store_1 = input("Are you sure? It is only one digit! (y / n)")
                if store_1 == 'y':
                    store_2 = input("Don't be silly! It's just one number! Add to the memory? (y / n)")
                    if store_2 == 'y':
                        store_3 = input("Last chance! Do you really want to embarrass yourself? (y / n)")
                        if store_3 == 'y':
                            M = result
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                        elif store_3 == 'n':
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                    elif store_2 == 'n':
                        choose = input('Do you want to continue calculations? (y / n):')
                        if choose == 'y':
                            continue
                        elif choose == 'n':
                            break
                elif store_1 == 'n':
                    choose = input('Do you want to continue calculations? (y / n):')
                    if choose == 'y':

                        continue
                    elif choose == 'n':
                        break
            elif store == 'y' and (result % 1 != 0 or (len(str(int(result))) > 1)) == True:
                M = result
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break
            elif store == 'n':
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break
        elif oper == '*':
            result = float(x) * float(y)
            print(result)
            store = input('Do you want to store the result? (y / n):')

            if (store == 'y' and result % 1 == 0 and len(str(int(result))) == 1) == True:
                store_1 = input("Are you sure? It is only one digit! (y / n)")
                if store_1 == 'y':
                    store_2 = input("Don't be silly! It's just one number! Add to the memory? (y / n)")
                    if store_2 == 'y':
                        store_3 = input("Last chance! Do you really want to embarrass yourself? (y / n)")
                        if store_3 == 'y':
                            M = result
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                        elif store_3 == 'n':
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                    elif store_2 == 'n':
                        choose = input('Do you want to continue calculations? (y / n):')
                        if choose == 'y':
                            continue
                        elif choose == 'n':
                            break
                elif store_1 == 'n':
                    choose = input('Do you want to continue calculations? (y / n):')
                    if choose == 'y':

                        continue
                    elif choose == 'n':
                        break
            elif store == 'y' and (result % 1 != 0 or (len(str(int(result))) > 1)) == True:
                M = result
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break
            elif store == 'n':
                choose = input('Do you want to continue calculations? (y / n):')
                if choose == 'y':
                    continue
                elif choose == 'n':
                    break

        elif oper == '/':
            try:
                result = float(x) / float(y)
                print(result)
                store = input('Do you want to store the result? (y / n):')

                if (store == 'y' and result % 1 == 0 and len(str(int(result))) == 1) == True:
                    store_1 = input("Are you sure? It is only one digit! (y / n)")
                    if store_1 == 'y':
                        store_2 = input("Don't be silly! It's just one number! Add to the memory? (y / n)")
                        if store_2 == 'y':
                            store_3 = input("Last chance! Do you really want to embarrass yourself? (y / n)")
                            if store_3 == 'y':
                                M = result
                                choose = input('Do you want to continue calculations? (y / n):')
                                if choose == 'y':
                                    continue
                                elif choose == 'n':
                                    break
                            elif store_3 == 'n':
                                choose = input('Do you want to continue calculations? (y / n):')
                                if choose == 'y':
                                    continue
                                elif choose == 'n':
                                    break
                        elif store_2 == 'n':
                            choose = input('Do you want to continue calculations? (y / n):')
                            if choose == 'y':
                                continue
                            elif choose == 'n':
                                break
                    elif store_1 == 'n':
                        choose = input('Do you want to continue calculations? (y / n):')
                        if choose == 'y':

                            continue
                        elif choose == 'n':
                            break
                elif store == 'y' and (result % 1 != 0 or (len(str(int(result))) > 1))  == True:
                    M = result
                    choose = input('Do you want to continue calculations? (y / n):')
                    if choose == 'y':
                        continue
                    elif choose == 'n':
                        break
                elif store == 'n':
                    choose = input('Do you want to continue calculations? (y / n):')
                    if choose == 'y':
                        continue
                    elif choose == 'n':
                        break
            except ZeroDivisionError:
                # print(f'{x}/{y}')
                print("Yeah... division by zero. Smart move...")
                continue
    elif (x_type and y_type) == False:
        print("Do you even know what numbers are? Stay focused!")
        continue
    elif oper not in ['+','-','*','/']:
        print ("Yes ... an interesting math operation. You've slept through all classes, haven't you?")
        continue
