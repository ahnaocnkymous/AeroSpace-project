
![isro-aircraft](https://github.com/user-attachments/assets/e23a3d47-e28c-4c9c-b685-a4574affb230)

each Functions uses thermodynamics first try to understand code u have know basics of thermodynamics!

def calculate_range(fuel_capacity, fuel_consumption_rate, true_air_speed): 
    range_in_hours = fuel_capacity/ fuel_consumption_rate 
    range_in_miles = range_in_hours * true_air_speed
    return range_in_miles

def calculate_endurance(fuel_capacity, fuel_consumption_rate):
    endurance_in_hours = fuel_capacity / fuel_consumption_rate
    return endurance_in_hours

def calculate_total_weight(payload, fuel_weight):
    total_weight_in_kg = math.ceil((payload + fuel_weight) / 2.2046) # weight in kg
    return total_weight_in_kg
    # if u want total weight in pounds remove the math.ceil code and use simply payload and fuel weight code
def calculate_cg_position(moment_list, total_weight):
    total_moment = sum(moment_list)
    cg_position = total_moment / total_weight
    return cg_position

def calculate_moment(weight, arm):
    return weight * arm

def calculate_lift(cl, rho, v, s):
    return 0.5 * cl * rho * v**2 * s

def calculate_drag(cd, rho, v, s):
    return 0.5 * cd * rho * v**2 * s
    
def calculate_weight(mass, g):
    return mass * g
    
def calculate_acceleration(thrust, drag, weight, mass):
    return(thrust - drag - weight) / mass

def calculate_velocity(velocity, acceleration, time):
    return velocity + acceleration * time

def calculate_distance(velocity, time):
    return velocity * time
