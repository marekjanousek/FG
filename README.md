# Program 1 (python)

import random

def number_guessing():
    secret_number = random.randint(1, 100)
    attempts = 0
    print("Guess a number between 1 and 100!")

    while True:
        guess = int(input("Your guess: "))
        attempts += 1

        if guess < secret_number:
            print("Try a higher number!")
        elif guess > secret_number:
            print("Try a lower number!")
        else:
            print(f"Congratulations! You guessed the number {secret_number} in {attempts} attempts.")
            break

number_guessing()

# Program 2 (python)

def calculator():
    print("Simple Calculator")
    number1 = float(input("Enter the first number: "))
    operation = input("Enter an operation (+, -, *, /): ")
    number2 = float(input("Enter the second number: "))

    if operation == '+':
        result = number1 + number2
    elif operation == '-':
        result = number1 - number2
    elif operation == '*':
        result = number1 * number2
    elif operation == '/':
        if number2 == 0:
            result = "Cannot divide by zero!"
        else:
            result = number1 / number2
    else:
        result = "Invalid operation"

    print("Result:", result)

calculator()


# Program 3 (python)


def count_vowels(text):
    vowels = "aeiouAEIOU"
    count = 0
    for char in text:
        if char in vowels:
            count += 1
    return count

# User input
user_text = input("Enter a sentence: ")
vowel_count = count_vowels(user_text)

print(f"The number of vowels in your text is: {vowel_count}")
