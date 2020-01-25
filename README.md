# guessgame
import random
import time
ls = ["R","P","S"] 
def random_generator():
    return random.choice(ls)

def checker():
    usr_sr = 0
    comp_scr = 0

    while usr_sr<5 and comp_scr<5:
        comp = random_generator()
        print(comp)
        usr = input("Type your input here-----")
        if usr == 'R' and comp == 'P':
            print("Compuer wins the match")
            
            comp_scr+=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == "P" and comp == "R":
            print("User wins the match")
            usr_sr +=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == "P" and comp == "S":
            print("computer wins the match")
            comp_scr+=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == "S" and comp == "P":
            print("User wins the match")
            usr_sr+=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == "R" and comp == "S":
            print("User wins the match")
            usr_sr+=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == "S" and comp == "R":
            print("computer wins the match")
            comp_scr+=1
            print(f"Score is: usr({usr_sr}) and computer({comp_scr})")
        elif usr == comp:
            print("Both choose the same thing.No score is added.")
        else: 
            print("Not a valid option.")
            continue
    print("calculating the score......")\
    time.sleep()
    ls = [usr_sr,comp_scr]
    print(f"The winner is {max(ls)} where usr_scr is {usr_sr} and computer score is {comp_scr}")    
        
        
        


if __name__ == "__main__":
    print("Welcome to rock, paper, secissor game. ")
    print("You have to select one among these three..")
    print("Select R for rock,P for paper, and S for secissor.")
    checker()
