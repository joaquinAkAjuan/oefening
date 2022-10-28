import os
import time

class color:
   BOLD = '\033[1m'
   UNDERLINE = '\033[4m'
   END = '\033[0m'


winkelwagentje = []
while True:
    print("\n")
    print(color.BOLD + 'dit is je winkelwagentje' + color.END)
    print("""
    wil je iets toevoegen  (t)
    of verwijderen  (v)
    of misschien je lijstje bekijken  (b)""")
    answer = input()
    if answer == "t":
        print("wat wil je toevoegen:")
        answer2 = input()
        winkelwagentje.append(answer2)
        print("\n")
        print(winkelwagentje)
        time.sleep(2)
        os.system("clear")
    if answer == "v":
        print("wat wil je verwijderen?")
        answer3 = input()
        winkelwagentje.remove(answer3)
        print("\n")
        print(winkelwagentje)
        time.sleep(2)
        os.system("clear")
    if answer == "b":
        print(winkelwagentje)