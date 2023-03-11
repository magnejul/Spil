# Spil
import random

# set up the game variables
score = 0
num_attempts = 5
target_location = random.randint(1, 10)

# define the game loop
while num_attempts > 0:
    # get the player's guess
    guess = input("Guess where the target is (1-10): ")
    guess = int(guess)
    
    # check if the guess is correct
    if guess == target_location:
        print("You caught the target!")
        score += 1
        num_attempts -= 1
        target_location = random.randint(1, 10)
    else:
        print("You missed!")
        num_attempts -= 1
    
    # show the current score and attempts remaining
    print("Score:", score)
    print("Attempts left:", num_attempts)

# show the final score
print("Game over! Your final score was:", score)
