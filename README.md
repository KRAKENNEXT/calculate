


def calculator():
    numbers = []
    num = int(input("Введите количество чисел: "))

    for i in range(num):
        number = float(input(f"Введите число {i+1}: "))
        numbers.append(number)

    operations = input("Введите последовательность операций (+, -, *, /) без пробелов: ")

    result = numbers[0]
    for i in range(1, len(numbers)):
        operation = operations[i-1]

        if operation == '+':
            result += numbers[i]
        elif operation == '-':
            result -= numbers[i]
        elif operation == '*':
            result *= numbers[i]
        elif operation == '/':
            if numbers[i] != 0:
                result /= numbers[i]
            else:
                print("Ошибка: деление на ноль.")
        else:
            print("Неверная операция:", operation)

    print("Результат:", result)

# Пример использования
calculator()

