# Python-Program-for-Octal-To-Binary-Conversion

Octal To Binary Conversion in Python
Here, in this page we will discuss the program for octal to binary conversion in Python . Numbers with base 8 are called octal numbers and uses digits from 0-7 for representation of octal number. Where as numbers with base 2 are called binary numbers  and it uses 0 and 1 for representation of binary numbers.

Algorithm for octal to binary conversion

Method 1:-
Accept octal number
Convert it into decimal Equivalent
Convert this decimal value into Binary
Make sure you have visited these two pages before moving ahead with the code –

Octal to Decimal conversion
Decimal to Binary Conversion
Method 1 Code in Python
Run
def convert(octal):
    i = 0
    decimal = 0
    while octal != 0:
        digit = octal % 10
        decimal += digit * pow(8, i)
        octal //= 10
        i += 1
    print("Decimal Value :", decimal)
    binary = 0
    rem = 0
    i = 1

    while decimal != 0:
        rem = decimal % 2
        decimal //= 2
        binary += rem * i
        i *= 10
    print("Binary Value :", binary)


octal = int(input("Octal Value : "))
convert(octal)
Output
Octal Value: 12
Decimal Value: 10
Binary Value: 1010
Related Pages
Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Permutations in which n people can occupy r seats in a classroom 

Octal to Binary conversion

Quadrants in which a given coordinate lies

Method 2
Each digit of an octal number can be converted into its binary Equivalent (see image)

Binary Representation for Octal digit:
0 => 000
1 => 001
2 => 010
3 => 011
4 => 100
5 => 101
6 => 110
7 => 111
Octal to Binary in C Program
Method 2 Code in Python
Run
def convert(octal):
    print("Equivalent Binary Number: ", end="")
    for i in range(len(octal)):
        switcher = {
            0: "000",
            1: "001",
            2: "010",
            3: "011",
            4: "100",
            5: "101",
            6: "110",
            7: "111"
        }
        print(switcher.get(int(octal[i]), "Invalid Octal Number"), end="")


octal = list(input("Insert an octal number: "))
convert(octal)
Output
Insert an octal number: 347
Equivalent Binary Number: 011100111
