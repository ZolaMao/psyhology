# psyhology
import time
import random

# List of colors
colors = ["red", "blue", "green", "yellow"]

def stroop_test():
    print("Welcome to the Stroop Test!")
    print("Type the color of the word, not the word itself.")
    print("Press 'q' to quit.")

    correct_answers = 0
    total_questions = 0
    start_time = time.time()

    while True:
        word = random.choice(colors)
        color = random.choice(colors)

        # Print the word in the chosen color
        print("\n" + word.upper() + " (in " + color + ")")
        response = input("Enter the color: ").lower()

        if response == color:
            print("Correct!")
            correct_answers += 1
        elif response == 'q':
            break
        else:
            print("Incorrect! The correct color was:", color)

        total_questions += 1

    end_time = time.time()
    time_taken = end_time - start_time

    print("\nTest finished!")
    print("You answered", correct_answers, "out of", total_questions, "questions correctly.")
    print("Time taken:", round(time_taken, 2), "seconds")

# Run the test
stroop_test()
