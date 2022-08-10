# rock-paper-scissor
import random
user_score = 0
computer_score =0
options = ["rock", "paper", "scissor"]
while True:
    user = input("Select Rock/Paper/Scissor or Q to quit:")
    if user == "Q":
        break
    if user not in options:
        print("enter correctt")
        continue
    computer = random.choice(options)
    print("computer choice:",computer)
    if(user == "rock" and computer == "scissor" or user == "scissor" and computer == "paper" or user == "paper" and computer == "rock"):
        print("user wins!!")
        user_score+= 1
    else:
        print("Computer wins!!")
        computer_score+=1
    if user == computer:
        print("tie")
   

print("you won",user_score,"times")
print("computer won",computer_score,"times")
