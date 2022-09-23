# predicting-of-the-molar-volume
 predicting of the molar volume by using the van der Waals equation ( It help to define the physical state of a real gas).
import numpy as np
# Given data
a = float(input("Veuillez saisir la valeur de a (l^2*atm/mol) : "))
b = float(input("Veuillez saisir la valeur de b (l/mol) : "))
T = float(input("Veuillez saisir la valeur de T (k)  : "))
P = float(input("Veuillez saisir la valeur de P(atm) : "))
# Constants
R = 0.082  # in l*atm/k*mol
# Calculate molar volume
V = [P, -P * b - R * T, a, -a * b]
sol = np.roots(V)
print("le volume molaire est :" ,sol[0].real," litres")
