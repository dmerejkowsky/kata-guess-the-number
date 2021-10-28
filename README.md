# Guess the number

*Goal: Implement a "guess the number" game matching the Specifications
below*

This kata is a good one to follow if you're new to programming.


# Specifications

Here's what the program should do when ran:

Draw a random number between 1 and 100 (called *the secret number*)

Start a loop

At each iteration of the loop:

  * Print "Guess the number!"
  * Halt the program until the user enters a number and presses enter
  * Read the user input (called *the guess*)
  * If the guess is greater than the secret, output "Too big"
  * If the guess is lower than the secret, output "Too small"
  * Otherwise, output "Win!" and exit the loop


# Hints

Since implementing the game from scratch requires a few concepts we did not cover yet,
you can use the following hints.

## Read user input

The following code halts the program until the user enters an input and
presses enter:

```python
user_input = input()
```

The variable `user_input` is then assigned to a **string** containing the user input.

## Draw a number at random


The following code assigns a random value between 1 and 6 to
the value "dice" - the value is hard to predict and
may change every time the code is executed

```python
import random
dice = random.randint(1, 6)
```


# If it's too easy

Only let the user make 10 tries at most and display the number of tries left at
each step.

# If it's too hard

You may start with the following skeleton:

```python
import random

secret_number = random.randint(0, 100)
print("the secret number is", secret_number)

print("Guess the number!")

user_input = input()
guess = int(user_input)

while True:
    if guess == secret_number:
        print("Win!")
        break
    else:
        print("Wrong answer :(")
        user_input = input()
        guess = int(user_input)
```

This code should run fine but has two problems:

First, it prints the secret number right away, which is too easy.

Second, the only information the user gets when he did not guess the correct
number is "Wrong answer :(",  which means the game is actually very hard to
play when the first problem is fixed ...

Try and correct the code to match the Specifications above.
