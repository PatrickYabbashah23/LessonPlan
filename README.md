# LessonPlan
#This Program simulates a Physics lesson plan for the upcoming semester

train_mass = 22680
train_acceleration = 10
train_distance = 100

bomb_mass = 1

#Converts Fahrenheit to Celsius

def f_to_c(f_temp):
  c_temp = f_temp - 32 * 5/9
  return c_temp
 
#Converts the tempture of 100 degrees Fahrenheit to Celsius by calling the f_to_c function

f100_in_celsius = f_to_c(100)
print(f100_in_celsius)

#Converts Celsius to Fahrenheit

def c_to_f(c_temp):
  f_temp = c_temp * 5/9 + 32
  return f_temp

##Converts the tempture of 0 degrees Celsius to Fahrenheit by calling the c_to_f function

c0_in_fahrenheit = c_to_f(0)
print(c0_in_fahrenheit)

#A function that calculates the mass times acceleration 
def get_force(mass, acceleration):
  return mass * acceleration

#Calculates and prints the force of a moving train based off the mass and acceleration based of the globalized variebles at the top of the program

train_force = get_force(train_mass, train_acceleration) 
print("The GE train supplies " +  str(train_force) + " Newtons of force.")

#A function that calculates the mass and the constant c which is set to the defult equation for the speed of light

def get_energy(mass, c=3*10**8):
  return mass * c**2

#Calculates and prints the energy levels of a bomb based of the global variables 

bomb_energy = get_energy(bomb_mass)
print("A 1kg bomb supplies " + str(bomb_energy) + " Joules.")

#A function that calculates the distance

def get_work(mass, acceleration, distance):
  return get_force(mass, acceleration) * distance

train_work = get_work(train_mass, train_acceleration, train_distance)
print("The GE train does " + str(train_work) + " Joules of work over " + str(train_distance) + " meters.")
  
  
