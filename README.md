# Stone-Paper-game
Develop a python program which prompts user to enter rock/paper/scissor and displays win or lose. Basically you have to develop a rock, paper, scissor game.
import random
#Stone-Paper-game
def play_rock_paper_scissors():
  """Plays a game of rock, paper, scissors."""

  while True:
    # Get user's choice
    user_choice = input("Enter your choice (rock, paper, scissors) or 'q' to quit: ").lower()
    if user_choice == 'q':
      break
    while user_choice not in ["rock", "paper", "scissors"]:
      print("Invalid choice. Please enter rock, paper, or scissors.")
      user_choice = input("Enter your choice (rock, paper, scissors) or 'q' to quit: ").lower()

    # Get computer's choice
    computer_choice = random.choice(["rock", "paper", "scissors"])

    print(f"You chose {user_choice}.")
    print(f"Computer chose {computer_choice}.")

    # Determine the winner
    if user_choice == computer_choice:
      print("It's a tie!")
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "scissors" and computer_choice == "paper") or \
         (user_choice == "paper" and computer_choice == "rock"):
      print("You win!")
    else:
      print("You lose!")

    print()

play_rock_paper_scissors()
