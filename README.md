import datetime
import random
import json

def generate_data():
    return {
        "timestamp": datetime.datetime.now().isoformat(),
        "random_value": random.randint(1, 1000)
    }

def save_data(data):
    with open("daily_output.json", "w") as f:
        json.dump(data, f, indent=4)

if __name__ == "__main__":
    new_data = generate_data()
    save_data(new_data)
    print("Daily data generated and saved:", new_data)
