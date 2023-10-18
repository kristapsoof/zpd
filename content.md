## Izveidot number guessing game ar pythonu programeesanas valodu

### Dokumenta saturs

### 1. Spēles apraksts
Interesanta spēle, kas attīsta loģiku
### 2. Spēles loģika

Datorus ģenerē vienu skaitli no 1 - 100. Tālāk, piedāvā spēlētājam uzminēt to skaitli.

Spēle notiek pēc šī koda:
```py
import random

number = random.randint(1, 100)
guess = 0
tries = []

while guess != number:
    if guess < number:
        print("Pamēģini lielāku skaitli.")
    else:
        print("Pamēģini mazāku skaitli.")

    guess = int(input("Uzmini skaitli: "))
    tries.append(guess)
else:
    print(f"You won from {len(tries)} tries!")
    print("heres your guessing history:")
    print(tries)
    
    sum_of_difference = 0
    
    for t in tries:
        sum_of_difference += abs(t-number)
        
    print(f"average difference was {sum_of_difference/len(tries)}")
```
