import random
import time
class Accelerometer:
    def __init__(self):
        self.acceleration = 0.0

    def read_acceleration(self):
        self.acceleration = random.uniform(-10.0, 10.0)
        return self.acceleration

class GPSModule:
    def __init__(self):
        self.latitude = 0.0
        self.longitude = 0.0

    def read_location(self):
        self.latitude = random.uniform(-90.0, 90.0)
        self.longitude = random.uniform(-180.0, 180.0)
        return self.latitude, self.longitude


class AccidentDetectionSystem:
    def __init__(self):
        self.accelerometer = Accelerometer()
        self.gps_module = GPSModule()
        self.threshold = 5.0  # Example threshold for acceleration that indicates a possible accident

    def detect_accident(self):
        acceleration = self.accelerometer.read_acceleration()
        if abs(acceleration) > self.threshold:
            return True
        return False

    def get_location(self):
        return self.gps_module.read_location()

    def send_alert(self, location):
        latitude, longitude = location
        alert_message = f"Accident detected! Location: Latitude {latitude}, Longitude {longitude}"
        print(alert_message)

        # Simulate sending alert
        print("Simulating sending alert to emergency services...")
        print("Alert sent successfully!")


def main():
    system = AccidentDetectionSystem()
    while True:
        if system.detect_accident():
            location = system.get_location()
            system.send_alert(location)
        time.sleep(1)  # Simulating a delay between sensor readings


if __name__ == "__main__":
    main()
