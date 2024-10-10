# final-python-project
import time

class YogurtProduction:
    def __init__(self):
        self.milk_amount = 0
        self.sugar_amount = 0
        self.preservative_amount = 0
        self.mixed = False

    def ration_milk(self, amount):
        # Code to control the milk pump
        self.milk_amount = amount
        print(f"Milk rationed: {amount} liters")

    def ration_sugar(self, amount):
        # Code to control the sugar dispenser
        self.sugar_amount = amount
        print(f"Sugar rationed: {amount} grams")

    def ration_preservatives(self, amount):
        # Code to control the preservative dispenser
        self.preservative_amount = amount
        print(f"Preservatives rationed: {amount} grams")

    def mix_ingredients(self):
        # Code to control the mixer
        print("Mixing ingredients...")
        time.sleep(5)  # Simulating mixing time
        self.mixed = True
        print("Ingredients mixed successfully")

    def measure_and_package(self, batch_size, num_batches):
        if not self.mixed:
            print("Error: Ingredients not mixed yet!")
            return
        for i in range(num_batches):
            # Code to control the packaging machine
            print(f"Batch {i+1}: Packaged {batch_size} liters of yogurt")
            time.sleep(2)  # Simulating packaging time

def main():
    production = YogurtProduction()

    # Ration milk, sugar, and preservatives
    production.ration_milk(100)  # Ration 100 liters of milk
    production.ration_sugar(10)  # Ration 10 grams of sugar
    production.ration_preservatives(5)  # Ration 5 grams of preservatives

    # Mix ingredients
    production.mix_ingredients()

    # Measure and package yogurt
    production.measure_and_package(batch_size=1, num_batches=100)  # Package 100 batches of 1 liter each

if __name__ == "__main__":
    main()
