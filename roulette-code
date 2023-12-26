import random

def randomizer(x):
  x = random.randrange(0, 38)
  return x


def select_bet(text):
  betno = []
  if text == "Inside":
    print("Valid inside bets: Straight, Street, Six-Line, and Top Line.")
    bet = input("Place a bet: ")
    if bet == "Straight":
      bet_number = int(input("Select a number between 00 and 36. Type 37 for 00. "))
      if not 0 <= bet_number <= 37:
        print("Invalid bet.")
        return betno
      betno.append(bet_number)
    elif bet == "Street":
      print("You will input the final number in your street bet.")
      print("This is a multiple of 3 from 3 to 36.")
      bet_number = int(input("Select the final number in your street bet: "))
      if bet_number == 3:
          bet_number = 1, 2, 3
      elif bet_number == 6:
          bet_number = 4, 5, 6
      elif bet_number == 9:
          bet_number = 7, 8, 9
      elif bet_number == 12:
          bet_number = 10, 11, 12
      elif bet_number == 15:
          bet_number = 13, 14, 15 
      elif bet_number == 18:
          bet_number = 16, 17, 18
      elif bet_number == 21:
          bet_number = 19, 20, 21
      elif bet_number == 24:
          bet_number = 22, 23, 24
      elif bet_number == 27:
          bet_number = 25, 26, 27
      elif bet_number == 30:
          bet_number = 28, 29, 30  
      elif bet_number == 33:
          bet_number = 31, 32, 33
      elif bet_number == 36:
          bet_number = 34, 35, 36
      else:
        print("Invalid bet.")
        return betno
      betno.append(bet_number)  
    elif bet == "Six-Line":
      print("You will input the final number in your six-line bet.")
      print("This bet will be on six numbers. These will form two consecutive lines.")
      print("You will select the final number in the six-line bet.")
      print("This will be a multiple of 3 starting from 6.")
      print()
      bet_number = int(input("Select the final number in your six-line bet (6-36): "))
      if bet_number == 6:
        bet_number = 1, 2, 3, 4, 5, 6
      elif bet_number == 9:
        bet_number = 4, 5, 6, 7, 8, 9
      elif bet_number == 12:
        bet_number = 7, 8, 9, 10, 11, 12
      elif bet_number == 15:
        bet_number = 10, 11, 12, 13, 14, 15
      elif bet_number == 18:
        bet_number = 13, 14, 15, 16, 17, 18
      elif bet_number == 21:
        bet_number = 16, 17, 18, 19, 20, 21
      elif bet_number == 24:
        bet_number = 19, 20, 21, 22, 23, 24
      elif bet_number == 27:
        bet_number = 22, 23, 24, 25, 26, 27
      elif bet_number == 30:
        bet_number = 25, 26, 27, 28, 29, 30
      elif bet_number == 33:
        bet_number = 28, 29, 30, 31, 32, 33
      elif bet_number == 36:
        bet_number = 31, 32, 33, 34, 35, 36
      else:
        print("Invalid bet.")
        return betno
      betno.append(bet_number)
    elif bet == "Top Line":
      bet_number = 0, 1, 2, 3, 37
      betno.append(bet_number)
  elif text == "Outside":
    print("You cannot bet a column bet.")
    print("Valid outside bets: High, Low, Red, Black, Dozen, Snake")
    bet = input("Select an outside bet: ")
    if bet == "Low":
      bet_number = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18
      betno.append(bet_number)
    elif bet == "High":
      bet_number = 19,20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36
      betno.append(bet_number)
    elif bet == "Red":
      bet = 1, 3, 5, 7, 9, 12, 14, 16, 18, 19, 21, 23, 25, 27, 30, 32, 34, 36
      betno.append(bet)
    elif bet == "Black":
      bet = 2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35
      betno.append(bet)
    elif bet == "Dozen":
      bet = (input("First, Second, or Third Dozen? Answer with 1st, 2nd, or 3rd. "))
      if bet == "1st":
        bet_number = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12
      elif bet == "2nd":
        bet_number = 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24
      elif bet == "3rd":
        bet_number = 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36
      else:
        print("Invalid dozen.")
        return betno
      betno.append(bet_number)
    elif bet == "Snake":
      bet = 1, 5, 9, 12, 14, 16, 19, 23, 27, 30, 32, 34
      betno.append(bet)
    else:
      print("Invalid bet.")  
      return betno
  else:
    print("Invalid bet.")
  return betno


def checkbet(x, y):
  for bet in x:
    if randomizer(y) in x:
      print(f"Yay! Your bet was correct! The ball landed on {randomizer(y)}.")
    else:
      print(f"Sorry, your bet was incorrect. The ball landed on {randomizer(y)}.")

print("You are playing roulette.")
print()
print("An outside bet is a bet of a wide range of numbers.")
print("An inside bet is a bet on a more specific range of numbers.")
print()
print("DISCLAIMER: This is an American-style roulette table.") 
print("If you see a number land on 37, this is substituting for 00.")
print()
bettype = input("Select a bet type - Inside or Outside: ")
betno = select_bet(bettype)
randnum = 0
checkbet(betno, randnum)
