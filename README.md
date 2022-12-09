# Roman-Number-to-integers 
# Python 

# Python program to convert roman number to integer

take=int(input('How many times you want to convert roman number: '))
char=0
while(char<take):
    def roman_to_int(s):
        rom_val = {'I': 1, 'V': 5, 'X': 10, 'L': 50, 'C': 100, 'D': 500, 'M': 1000}
        value = 0
        for i in range(len(s)):
            if i > 0 and rom_val[s[i]] > rom_val[s[i - 1]]:
                value += rom_val[s[i]] - 2 * rom_val[s[i - 1]]
            else:
                value += rom_val[s[i]]
        return value
    char+=1

    a=input('Enter the roman numbers(in caps): ')
    print('After converting into integer:',roman_to_int(a))
