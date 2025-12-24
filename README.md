# random_game
import os
import hashlib

FILE = ("SIAM")

def hash_pass(p):
    return hashlib.sha256(p.encode()). hexdigest()

def user_exists(u):
    if not os.path.exists(FILE):
        return False
    with open(FILE, "r") as f:
        for line in f:
            name, _ = line.strip().split("|")
            if name == u:
                return True
    return False
# ========= REGISTER ========= 
def register():
    os.system("cls" if os.name == "nt" else "clear")
    print("===== REGISTER =====")
    u = input("Username: ")
    if user_exists(u):
        print("User already exists!")
        input("Enter...")
        return

    p1 = input("Password: ")
    p2 = input("Confirm Password: ")

    if p1 != p2:
        print("Password mismatch!")
        input("Enter...")
        return

    with open(FILE, "a") as f:
        f.write(u + "|" + hash_pass(p1) + "\n")

    print("Registration Successful!")
    input("Enter...")
#register()
# ========= LOGIN =========
def login():
    
    os.system
    print("===== LOGIN =====")
    u = input("Username: ")
    p = input("Password: ")
    hp = hash_pass(p)

    if u != os.path.exists(FILE):
        print("No users found!")
        input("Enter...")
    if u == os.path.exists(FILE):
        print ("successful")  
        input ("Enter.......")
    if p != os.path.exists(FILE):
        print("No users found! ")  
    if p == os.path.exists(FILE):
        print ("successful")
        
    

def dashboard(user):
    while True:
        os.system("cls" if os.name == "nt" else "clear") 
        
        
   
 #random game ;       
def random():
    for i in range (2):
            import random 
            import os
            numbar = random.randint(1,10)
            guess = input(" guess the numbar betowen 1     to 10 -::-: ")
            guess = int(guess)

            if guess == numbar :
                print ('you are win ',numbar)
            else:
                 print ('the lacky numbar is : ',numbar)
    


register()
login()
hash_pass('p')
random()
 
