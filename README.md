# Project-Raspberry-Servo-motor
This project was developed academically for learning purposes.

-	Components 
Raspberry 
1 Protoboard
1 Led 
Servo motor
4 cables (m/f)
1 resistor

-	Creating code in Thonny software
#

import RPi.GPIO as GPIO
import time

# Defines the GPIO port that will be used
GPIO.setmode(GPIO.BOARD)
GPIO.setup(11,50)
servo= GPIO.PWM(11,50)
GPIO.setup(13, GPIO.OUT)

# Infinite loop to keep the LED on
while True:
    GPIO.output(13, GPIO.HIGH)
    time.sleep(1)  # intervalo de 1 segundo
    GPIO.output(13, GPIO.LOW)
    time.sleep(1)  # intervalo de 1 segundo
    servo.start(0)
    servo.ChangeDutyCycle(7.5)
    time.sleep(1)
    servo.ChangeDutyCycle(12.5)
    time.sleep(1)
    
