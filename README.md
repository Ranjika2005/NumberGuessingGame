# NumberGuessingGame
The Number Guessing Game challenges users to guess a randomly generated number, enhancing logical reasoning.

import tkinter as tk
import random

def check_guess():
    guess = int(entry.get())
    if guess < number:
        result_label.config(text="Too low!")
    elif guess > number:
        result_label.config(text="Too high!")
    else:
        result_label.config(text="Correct! The number was " + str(number))

def new_game():
    global number
    number = random.randint(1, 100)
    result_label.config(text="Guess a number between 1 and 100")
      	root = tk.Tk()
root.title("Guess the Number Game")
instruction_label = tk.Label(root, text="Enter your guess:")
instruction_label.pack()
entry = tk.Entry(root)
entry.pack()
guess_button = tk.Button(root, text="Guess", command=check_guess)
guess_button.pack()

result_label = tk.Label(root, text="Guess a number between 1 and 100")
result_label.pack()

new_game_button = tk.Button(root, text="New Game", command=new_game)
new_game_button.pack()
new_game()
root.mainloop()


