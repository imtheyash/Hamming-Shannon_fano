# HUFFMAN AND SHANNON_FANO
# Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25,0.0625, 0.125, 0.125, 0.25} for its output.Apply the Huffman and Shannon-Fano to this source.
# AIM:
To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variancefor a discrete memoryless source using Huffman and Shannon-Fano coding based on thegiven probabilities and codeword lengths.
# TOOLS REQUIRED:
Python: A versatile language for scientific computing and signal processing.<br />
NumPy & Matplotlib: Libraries for numerical operations and high-quality visualizations,essential for demonstrating sampling.
# PROGRAM:
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
print(f"Variance is : {var}")
```
# OUTPUT:
![Screenshot 2025-03-25 191943](https://github.com/user-attachments/assets/dae25aec-9942-4f8f-9fd8-2312c48d7d27)

CALCULATIONS:
![WhatsApp Image 2025-04-08 at 10 39 44_2dc72159](https://github.com/user-attachments/assets/8b4fef54-eed7-4fec-9609-c326b81015b2)

![WhatsApp Image 2025-04-08 at 10 39 44_7e6c6978](https://github.com/user-attachments/assets/65d3fb26-1897-4a6f-996e-e3015a543dcc)

![WhatsApp Image 2025-04-08 at 10 39 45_4606e1aa](https://github.com/user-attachments/assets/a748d61a-d770-4822-bdd5-95ded6ec29e7)

# RESULT:
For the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25.<br />
Average Codeword Length is : 2.625<br />
Entropy is : 2.625<br />
Efficiency is : 100.0 %<br />
Redudancy is : 0.0<br />
Variance is : 0.484.<br />
