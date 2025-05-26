# Exerc-cio-2-Contando-movimento-da-ordena-o
import random

def insertionSort(gcbr_arr):
    gcbr_deslocamentos = 0
    for gcbr_i in range(1, len(gcbr_arr)):
        gcbr_chave = gcbr_arr[gcbr_i]
        gcbr_j = gcbr_i - 1
        while gcbr_j >= 0 and gcbr_arr[gcbr_j] > gcbr_chave:
            gcbr_arr[gcbr_j + 1] = gcbr_arr[gcbr_j]
            gcbr_deslocamentos += 1
            gcbr_j -= 1
        gcbr_arr[gcbr_j + 1] = gcbr_chave
    return gcbr_deslocamentos

def generate_random_array(gcbr_size, gcbr_min_val=1, gcbr_max_val=100):
    return [random.randint(gcbr_min_val, gcbr_max_val) for _ in range(gcbr_size)]

def main():
    gcbr_t = int(input())
    for _ in range(gcbr_t):
        gcbr_n = int(input())
        gcbr_arr = list(map(int, input().split()))
        gcbr_result = insertionSort(gcbr_arr)
        print(gcbr_result)

if __name__ == '__main__':
    main()

