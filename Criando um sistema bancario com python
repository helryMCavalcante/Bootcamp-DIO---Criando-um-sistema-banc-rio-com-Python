from time import sleep

menu=f"""
###### MENU #######
[d] Deposito
[s] Saque
[e] Extrato
[q] Sair
###################
==>"""

saldo= 0
limete= 500
extrato= ""
numero_saques= 0
LIMITE_SAQUES = 3

while True:
    opção = input(menu)

    if opção == "d":
        valor_deposito = float(input("Informe o valor que deseja depositar:"))
        if valor_deposito > 0:
            saldo+=valor_deposito
            print("Deposito realizado com sucesso!\n")
            extrato += f"Deposito: {valor_deposito:.2f}\n"
        else:
            print("Valor de deposito invalido")

        conti = str(input("Deseja continuar a operação? [S] - Sim // [N] - Não: ")).upper()
        if conti == 's'.upper():
            print("Saindo da operação...")
            sleep(1)
        else:
            break

    elif opção == "s":
        saque = float(input("Infome o valor que deseja sacar: R$ "))
        if saque > 0:
            if saldo >= saque and numero_saques < LIMITE_SAQUES:
                if saque <= 500:
                    saldo -= saque
                    print("Saque realizado com sucesso!")
                    numero_saques += 1
                    extrato += f"Saque: R${saque:.2f}\n"
                else:
                    print("Limite de saque excedido")
            elif saldo < saque:
                print("Você não possui saldo suficiente para o saque")
            else:
                print("Não é possivel sacar. Limite diario de 3 saques")
        else:
            print("Valor de saque invalido")

        conti = str(input("Deseja continuar a operação? [S] - Sim // [N] - Não: ")).upper()
        if conti == 's'.upper():
            print("Saindo da operação...")
            sleep(1)
        else:
            break


    elif opção == "e":
        print("############### EXTRATO ###############")
        print(extrato)
        print(f"Saldo atual: R${saldo:.2f}")
        print("#######################################")

    elif opção == "q":
        break

    else:
        print("Operação invalida! por favor selecione novamente a operação desejada.")
