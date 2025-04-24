import openmc

# Create material using atomic fractions
li_pe_atomic = openmc.Material(name='Li-Polyethylene (Atomic Fractions)')

# Add isotopes with atomic fractions
li_pe_atomic.add_nuclide('C12', 0.3075)
li_pe_atomic.add_nuclide('C13', 0.0031)
li_pe_atomic.add_nuclide('H1', 0.6196)
li_pe_atomic.add_nuclide('H2', 0.0000624)
li_pe_atomic.add_nuclide('Li6', 0.00609)
li_pe_atomic.add_nuclide('Li7', 0.0636)

# Adding the defined materials to the OpenMC model
model.materials = openmc.Materials([li_pe_atomic])
print(model.materials) 

# simulation Output 
[Material
	ID             =	1
	Name           =	Li-Polyethylene (Atomic Fraction)
	Temperature    =	None
	Density        =	None [sum]
	Volume         =	None [cm^3]
	Depletable     =	False
	S(a,b) Tables  
	Nuclides       
	C12            =	0.3075       [ao]
	C13            =	0.0031       [ao]
	H1             =	0.6196       [ao]
	H2             =	6.24e-05     [ao]
	Li6            =	0.00609      [ao]
	Li7            =	0.0639       [ao]
	Li7            =	0.0639       [ao]
	Li7            =	0.0639       [ao]
]
