# RPS-LEGEND-Rock-Paper-Scissors-Game
The Legend of RPS is a Python-based Rock-Paper-Scissors game where players compete against a bot to claim the title of "RPS Champ". Featuring a simple menu, fun gameplay, and dynamic score tracking, combined with a touch of drama and humor, to create an engaging user experience.
# HOW IT WORKS
1. Menu System:
The program starts with a main menu offering three options:
Start the Battle: Initiates the Rock-Paper-Scissors game loop.
Rules of the Arena: Displays the game rules.
Score & Title: Shows the current scores and determines the RPS Champ.

2. Gameplay Loop:
The player is asked to choose between Rock, Paper, or Scissors.
The program generates the RPS-Bot’s move using the random function.
The game compares the player’s choice with the bot’s and determines the winner using conditional logic.

3. Score Tracking:
Both the player’s and the bot’s scores are updated after each round.
A scoring system keeps track of the results throughout the session.

4. Outcome Display:
The program displays round results (win, lose, or draw) with fun and engaging messages.

5. Score & Title Section:
At any time, players can view their scores and check if they’ve dethroned the bot to become the RPS Champ.

# CODE
import random 
sc = 0 
cc = 0 
def gamestart(): 
 global sc, cc 
 while True: 
 user = input("Choose your weapon: rock, paper or scissors: ") 
 possible_actions = ["rock", "paper", "scissors"] 
 if user not in possible_actions: 
 print("Oops! You only have the above mentioned weapons :( Try again!\n") 
 continue 
 computer = random.choice(possible_actions) 
 print(f"\nYou chose {user}, computer chose {computer}.\n") 
 if user == computer: 
 print(f"Both players selected {user}. It's a tie!\n") 
 elif user == "rock": 
 if computer == "scissors": 
 sc += 1 
 print("Rock smashes Scissors into scrap! You win!\n")
 else: 
 cc += 1 
 print("Paper wraps Rock into submission! You lose.\n") 
 elif user == "paper": 
 if computer == "rock": 
 sc += 1 
 print("Paper wraps Rock into submission! You win!\n") 
 else: 
 cc += 1 
 print("Scissors cuts Paper into confetti! You lose.\n") 
 elif user == "scissors": 
 if computer == "paper": 
 sc += 1 
 print("Scissors cuts Paper into confetti! You win!\n") 
 else: 
 cc += 1 
 print("Rock smashes Scissors into scrap! You lose.\n") 
 play_again = input("Play again? (y/n): ") 
 if play_again.lower() == "y": 
 menu() 
 
 elif play_again.lower() == "n": 
 print("Your score is:", sc) 
 print("RPS-bot's score:", cc) 
 break
 def rules(): 
 print("""Rules of the Arena: 
1. Choose Your Weapon: 
Rock (The Crusher) 
Paper (The Wrapper) 
Scissors (The Slicer) 
2. The Power Moves: 
Rock smashes Scissors into scrap! 
Scissors cuts Paper into confetti! 
Paper wraps Rock into submission! 
If both choose the same weapon, it’s a draw—no points, just awkward eye contact. 
3. The Goal: Outsmart the RPS-Bot, win the most rounds, and take the crown.""") 
 menu() 
def menu(): 
 print("""WELCOME TO THE LEGEND OF RPS
For years, the legendary RPS-Bot has ruled as the undefeated RPS Champ, boasting an 
unbroken streak and a digital smirk that screams confidence. But now, it’s your turn to 
step into the arena and take it down. 
Your Mission: Dethrone the RPS-Bot and steal the title! But beware—this bot’s got tricks 
up its digital sleeves.""") 
 ch = int(input("""1. RULES OF THE ARENA 
2. START BATTLE 
3. SCOREBOARD OF GLORY 
Your choice: """)) 
 if ch == 1: 
 rules() 
 elif ch == 2: 
 gamestart() 
 elif ch == 3: 
 print("SCOREBOARD OF GLORY\n") 
 if sc > cc: 
 print(f"""You did it! Congratulations, you’re the new RPS Champ! The RPS-Bot 
never saw that coming! 
Your Score: {sc} 
RPS-Bot’s Score: {cc} 
You outsmarted the bot and claimed the crown! Well played, champion!""") 
 elif sc < cc:
print(f"""Oh no! The RPS-Bot reigns supreme once again! You gave it your all, but 
this time, the bot takes the title.
Your Score: {sc}
RPS-Bot’s Score: {cc}
Better luck next time, hero. The bot remains the unchallenged RPS Champ!""")
menu()
____________________

