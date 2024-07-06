# Password Hacking Exercise Helper

This repository is to be used in conjunction with [password-flask-app](https://github.com/pratt13/password-flask-app).
This creates some simple python scripts to help hit the expected endpoints, whether you are serving the target app locally or on replit.


This repository is a simple python repository to demonstrate how to:
a. Crack bad passwords using 2 obvious techniques.
b. Generate a strong(ish) password in python

## Requirements
## Setup
```sh
python3 -m venv password-helper
source password-helper/bin/activate
pip3 install -r requirements.txt
```

In main there is a section

```py
# Add the URL here you want to hack
# One time URL - change once during the exercise
BASE_URL = "http://localhost:5000"
```

If you are running the [flask app](https://github.com/pratt13/password-flask-app) locally then you do not need to change it.
If you are using the flask app on replit, you will need to change this to the address replit provides the flask app.

## The tasks

First thing to do is just ro run it
```sh
python3 main.py
```

This `should` give na error (`NotImplementedError`). 
This is because looking through `main.py` it is trying to run `boyles_task`.
Namely, trying to crack the UI address that is password protected by Boyle.
You need to go to `task1_boyle.py` and change what that function returns.
The flask app UI has some help if you get stuck.

As you progress through the exercises, then uncomment the lines fo code in `main.py`.
Eventually or the task should be uncommented and you can crack both `boyle's` and `terry's` passwords, as well as creating a function that makes one that is relatively string.


## Tasks
Summary of tasks are below, but the flask app has far more information of you navigate to it.
Locally, if run it will be on `localhost:5000` or on replit it will be the URL given.
### Task 1
#### Boyle's Task

Boyle has a web page with all his secrets, he has a password as a three digit pin. Can you guess it?

#### Terry's Task

Terry has a web page with all his secrets, he has a password that uses four common phrases, plus two extra characters.

## Task 2
Create a python function to generate a password of 8 characters.
It must have:
* A lowercase letter
* An uppercase letter
* A number
* A special character `£$?!_`
* No examples of `Qwerty, Password, Pa$$w0rd, yoghurt, cagney, lacey`
* No repeats within 100 tries
* Range of characters, not all the letter `a1a2a3a4`
* All characters are randomly and uniformly chosen.

## Testing
### Unit tests

```sh
python3 -m unittest
```
