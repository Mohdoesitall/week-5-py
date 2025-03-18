# questiion 1
# Parent Class
class Device:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def device_info(self):
        return f"Device: {self.brand} {self.model}"

# Child Class (Inheritance)
class Smartphone(Device):
    def __init__(self, brand, model, storage, battery):
        super().__init__(brand, model)  # Inherit from Device
        self.storage = storage
        self.__battery = battery  # Private Attribute (Encapsulation)

    def make_call(self, number):
        return f"Calling {number} from {self.brand} {self.model} 📱"

    def battery_status(self):
        return f"Battery: {self.__battery}% 🔋"

# Create an object
my_phone = Smartphone("Apple", "iPhone 14", "128GB", 85)

# Test methods
print(my_phone.device_info())
print(my_phone.make_call("123-456-7890"))
print(my_phone.battery_status())  


# question 2
class Vehicle:
    def move(self):
        pass  # Placeholder for subclasses

class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

class Boat(Vehicle):
    def move(self):
        return "Sailing ⛵"

# Create objects
vehicles = [Car(), Plane(), Boat()]

# Test polymorphism
for v in vehicles:
    print(v.move())
