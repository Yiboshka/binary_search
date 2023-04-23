scroll_numbers = input("Введите последовательность чисел через пробел: ")
user_num = int(input("Введите целое число для поиска: "))

if " " not in scroll_numbers:
    print("Водите только целые числа через пробел.")
    scroll_numbers = input('Введите последовательность чисел через пробел: ')
else:
    scroll_numbers = scroll_numbers.split()

scroll_numbers = scroll_numbers.split()
list_numbers = list(map(int, scroll_numbers))
array = list_numbers

def qsort(array, left, right):
    middle = (left + right) // 2
    p = array[middle]
    i, j = left, right
    while i <= j:
        while array[i] < p:
            i += 1
        while array[j] > p:
            j -= 1
        if i <= j:
            array[i], array[j] = array[j], array[i]
            i += 1
            j -= 1
    if j > left:
        qsort(array, left, j)
    if right > i:
        qsort(array, i, right)
    return array

qsort(list_numbers, 0, len(array)-1)

def binary_search(array, element, left, right):
    if left > right:
        try:
            return ('Введенного числа нет в последовательности.\n'
                    'Перезапустите программу и попробуйте снова.\n'
                    'Ближайшие имеющиеся числа:\n'
                    f'{array[right]} <индекс [{right}]>,\n'
                    f'{array[left]} <индекс [{left}]>')
        except IndexError:
            return ('Введенного числа нет в последовательности.\n'
                    'Перезапустите программу и попробуйте снова\n'
                    'Ближайшее число:\n'
                    f'{array[right]} <индекс [{right}]>')
    middle = (right+left) // 2
    if array[middle] == element:
        return (f'Ваше число {array[middle]} найдено с индексом [{middle}]\n'
                f'Предыдущее число {array[middle - 1]} с индексом [{middle - 1}]\n'
                f'Следующее число {array[middle + 1]} с индексом [{middle + 1}]')
    elif element < array[middle]:
        return binary_search(array, element, left, middle-1)
    else:
        return binary_search(array, element, middle+1, right)

binary_search(array, user_num, 0, len(array) - 1)
print(binary_search(array, user_num, 0, len(array) - 1))

