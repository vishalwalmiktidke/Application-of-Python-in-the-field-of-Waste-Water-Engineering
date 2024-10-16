# Application-of-Python-in-the-field-of-Waste-Water-Engineering
ASSIGNMENT NO. 09

Q.1) # To find the decay coefficient at 25°C
K1 = float(input("Enter the decay coefficient (K1): "))
T1 = float(input("Enter the temperature of 7th day BOD (T1): "))
T2 = 25.0  # Standard temperature for calculations
K2 = K1 * (1.047 ** (T2 - T1))
print("The value of K2 is:", K2)

# To find Ultimate BOD (L0)
print("The value of e (Euler's number) is:", math.e)
B1 = float(input("Enter BOD at 3rd day 20°C (B1): "))
t = float(input("Enter time in days for finding B1: "))
E = (1 - math.exp(-0.23 * t))
print("The value of E is:", E)
L0 = B1 / E
print("The value of L0 (Ultimate BOD) is:", L0)

# To find BOD at 7th day 25°C
t1 = float(input("Enter time in days for finding B2: "))
E1 = (1 - math.exp(0.289 * t1))
print("The value of E1 is:", E1)
B2 = L0 * E1
print("The value of B2 (BOD at 7th Day 25°C) is:", B2)

OUTPUT:
Enter the decay coefficient (K1): 0.23
Enter the temperature of 7th day BOD (T1): 25
The value of K2 is: 0.23
The value of e (Euler's number) is: 2.718281828459045
Enter BOD at 3rd day 20°C (B1): 20
Enter time in days for finding B1: 3
The value of E is: 0.49842393093394455
The value of L0 (Ultimate BOD) is: 40.126484221020625
Enter time in days for finding B2: 7
The value of E1 is: -6.560973864873026
The value of B2 (BOD at 7th Day 25°C) is: -263.2688142633562

Q.2) # Determination of density of sludge removed from aeration tank
M = float(input("Enter the value of initial mass (in kg): "))
S = float(input("Enter the value of solid containing sludge in percentage: "))
Gs = float(input("Enter the value of specific gravity of sludge solid: "))
Rho_W = float(input("Enter the value of density of water (in kg/m^3): "))

# Calculate the mass of solid in the sludge
Ws = (S / 100) * M  # Mass of solids in kg
m = M - Ws  # Mass of water in kg

print("The value of mass of water:", m, "kg")
print("The value of solid content in sludge:", Ws, "kg")

# Calculate the volume of water
Vw = m / Rho_W  # Volume of water in m^3
print("The value of volume of water:", Vw, "m^3")

# Calculate the density of solid content in sludge
Rho_S = Gs * Rho_W  # Density of solid content in kg/m^3
print("The value of density of solid content in sludge:", Rho_S, "kg/m^3")

# Calculate the volume of solid content in sludge
Vs = Ws / Rho_S  # Volume of solid content in m^3
print("The value of volume of solid content in sludge:", Vs, "m^3")

# Calculate total volume of sludge
Vt = Vw + Vs  # Total volume of sludge in m^3
print("The value of total volume of sludge:", Vt, "m^3")

# Calculate the density of sludge removed from aeration tank
Rho_SL = M / Vt  # Density of sludge in kg/m^3
print("The value of density of sludge removed from aeration tank:", Rho_SL, "kg/m^3")

OUTPUT:
Enter the value of initial mass (in kg): 100
Enter the value of solid containing sludge in percentage: 2
Enter the value of specific gravity of sludge solid: 2.2
Enter the value of density of water (in kg/m^3): 1000
The value of mass of water: 98.0 kg
The value of solid content in sludge: 2.0 kg
The value of volume of water: 0.098 m^3
The value of density of solid content in sludge: 2200.0 kg/m^3
The value of volume of solid content in sludge: 0.0009090909090909091 m^3
The value of total volume of sludge: 0.09890909090909092 m^3
The value of density of sludge removed from aeration tank: 1011.0294117647057 kg/m^3
