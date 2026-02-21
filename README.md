# NAME: AARTHI R
# REG NO: 212224060003
# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics  {0.4,0.2,0.2,0.1,0.1} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n):
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))
    p.append(pr)
for j in range (n):
    l = float(input(f"Enter the length of the sample values {j + 1}: "))
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy
red =  round(1 - eff,3)
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="1008" height="1600" alt="image" src="https://github.com/user-attachments/assets/b6dfc148-9d4e-42bc-be9d-0fafa69ea40a" />

<img width="1279" height="1600" alt="image" src="https://github.com/user-attachments/assets/18c54af5-0f9e-4a19-b232-0cde44ed8939" />

# Output
<img width="812" height="374" alt="image" src="https://github.com/user-attachments/assets/899a1e33-4408-4e6b-8658-2810dcbb336f" />
 
# Results:
The Huffman and Shannon-Fano of the given statistics {0.4,0.2,0.2,0.1,0.1} using python are verified.

