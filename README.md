# Python Countdown App

## Introduction
This Python Countdown App allows users to input a goal and a deadline, and it calculates and prints the remaining time until that deadline. It makes use of the datetime module for time calculation.

## Features
- Accepts user input for goal and deadline
- Calculates and prints the remaining time until the deadline
- Utilizes the datetime module for time calculations

## Prerequisites
- Python installed on your system

### Code

```python

from datetime import datetime

user_input = input("enter your goal with a deadline separated by a colon\n")
input_list = user_input.split(":")

goal = input_list[0]
deadline = input_list[1]

deadline_date = datetime.strptime(deadline, "%d.%m.%Y")
today_date = datetime.today()
time_till = deadline_date - today_date

hours_till = int(time_till.total_seconds() / 60 / 60)
print(f"Dear user! Time remaining for your goal: {goal} is {hours_till} hours")

# print(f"Dear user! Time remaining for your goal: {goal} is {time_till.days} days")
```

<img src="https://i.imgur.com/qlabn13.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
