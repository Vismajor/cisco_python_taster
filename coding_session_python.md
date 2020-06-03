# Coding Experience (Taster Session) - Building a Full Stack Application in 2 Hours

**Lesson Duration: 60 + 60 minutes**

> **Note to instructors: Read these notes once or twice and then just use them as visual clues. You'll need to use some of your own metaphors and explaining style**

## Intro

>	LEARNING GOALS:
>	- Know what programming is: metaphor of a TV program
>	- Difference between reading code and running (aka. executing, interpreting) code (like knowing how to clap vs clapping; "say: Hi Steve", "Hi Steve")

### Understand what programming is

What would you use the word 'program' in an everyday English? (let people give you answers)
Definitely a TV program (aka. schedule) is a great example:
- list of things that happen one after another ("Pokemon episode #312", "Eastenders episode #1004", etc)
- read from top to bottom, always happening in that order, nothing is skipped
- their value of lines in TV program is not in the name and the time slot. The value is what happens when that line is 'aired' or 'run' or 'executed'. That's when you actually go and watch your show

### Written code, Executed code

Today we will write our first computer programs. We will instruct the computer to do things from top to bottom and watch the computer execute each command. Just like when composing the TV program, we will write a set of commands (think of them as orders, requests or tasks) and then we will tell computer to interpret these lines of code as an actual actions.

Instruct everyone to:

- open terminal
- create a folder `mkdir coding`
- enter that folder `cd coding`
- create a file in that folder `touch names.py`
- open that file in atom editor `atom names.py` (here you can instruct everyone to use Tab button for completing the words)
- at this point instruct everyone to layout their computers in split screen. Code on left hand side, terminal on right hand side. (On a mac you do this by long-holding the green button on top left of the window, and while holding it, you drag it to the side of the screen, then select the other app to take up the rest of the screen.

Note: when they run the file, teach them to use arrow up and enter in terminal.

### Know what computers are good at

Throughout this lessons we will give computers tasks that computers are good at (eg. repeating things, remembering a lot of data) while avoiding tasks that computers are bad at (eg. creativity).

## Coding Part 1

## **Following Simple commands**


>  LEARNING GOALS:
>	- How to print (display) things to a screen (**print**)
>	- What are strings (basically they are words)(**"a string"**)
>	- assign values **=**

Say something simple. (print, stands for print a string of characters on screen)
Notice that the word "print" is not prInted on the screen. This is INTERPRETED!

```python
print('Hello World!')
```

We make computer do some work and then print the result. Notice that computer interprets things from right to left.

```python
print('Hello' + ' World!')
```

But as we said computers are easy to baffle, so it won't know what to do sometimes. Still it will try to communicate in their own clumsy way. Below will give us an error. But don't panic.

```python
print('Hello' + ' World!' + 2 + 2)
```

TypeError: can only concatenate str (not "int") to str
Oh dear, yes, let's fix it

```python
print(2 + 2)
```

Ok, rewind back to:

```python
print('Hello' + ' World!')
```


## **Remembering things**

>  LEARNING GOALS:
>	- Values can be stored in variables (assignment operator **=** )
>	- How to use variables in strings (**"#{variable}"**)

```python
greeting = 'Hello' + ' World!'
print(greeting)
```

Guide students through writing a simple theatre play:

```python
print("Rebecca: Hi, I'm Rebecca!")
print("James: Hi Rebecca, I'm James!")
print("Rebecca: Good to meet you James!")
```

something is not DRY (Don't Repeat Yourself). Names are repeated a lot. We could extract them to two variables, you have seen this already:

```python
person1 = "Rebecca"
person2 = "James"

print("Rebecca: Hi, I'm Rebecca!")
print("James: Hi Rebecca, I'm James!")
print("Rebecca: Good to meet you James!")

```

and now we can replace all occurrences of these names in our code:

```python
person1 = "Rebecca"
person2 = "James"

print("person1: Hi, I'm person1!")
print("person2: Hi person1, I'm person2!")
print("person1: Good to meet you person2!")

```

But this still does not work! Correct. Notice that things in brackets are in English (not Python) so do not get intepreted. We need to tell Python that when we say person1 we actually mean the VALUE stored in the variable person1 (which is Rebecca). We do this with 'comicbook swearing' syntax, aka. string interpolation. To make it happen, highlight a word in side of a string and press Shift+3   

```python
person1 = "Rebecca"
person2 = "James"

print(f"{person1}: Hi, I'm {person1}!")
print(f"{person2}: Hi {person1}, I'm {person2}!")
print(f"{person1}: Good to meet you {person2}!")
```

## **Logic**

>  LEARNING GOALS:
>	- How to make decisions based on simple logic (**if else**)
>	- directing code into side track (like a train) and returning to the main track (**end**)
>	- wait for user input (**input**)
>	- use user input to change code path (**input + if**)

Let's make our computer take some decisions!
When explaining if else, use the metaphor of train tracks detaching from main route and then returning to it (and point to indentation when you're doing it).

```python
person1 = "Rebecca"
person2 = "James"

print(f"{person1}: Hi, I'm {person1}!")
print(f"{person2}: Hi {person1}, I'm {person2}!")
if person1 == person2:
    print("Oh! our names are the same")
print(f"{person1}: Good to meet you {person2}!")
```

Run the code as is and then change both names to the same one and see what happens.
After adding ELSE, have students change values again. Here you can explain what TESTING is. that you should always aim top explore every possible route of action (each possible train route) so that you definitely know it works.


```python
person1 = "Rebecca"
person2 = "James"

print(f"{person1}: Hi, I'm {person1}!")
print(f"{person2}: Hi {person1}, I'm {person2}!")
if person1 == person2:
    print("Oh! our names are the same")
else:
    print("Oh! We have different names")
print(f"{person1}: Good to meet you {person2}!")
```


This whole value changing business is becoming cumbersome. Games would not be fun if all questions and answers were decided by the programmer when they write the code. Let's give some decisive powers to the USER, so in the part of the screen where we are RUNNING the code.

We want and then take some input from users. we'll use input. It gets a string from the screen, rather than print'ing it there.

```python

person1 = "Rebecca"
person2 = input("What's your name? ")

print(f"{person1}: Hi, I'm {person1}!")
print(f"{person2}: Hi {person1}, I'm {person2}!")
if person1 == person2:
    print("Oh! our names are the same")
else:
    print("Oh! We have different names")
print(f"{person1}: Good to meet you {person2}!")
```

play the game a few times. Make sure you reach each possible line of code

## TAKE A BREAK HERE

## **Repeating things**

>  LEARNING GOALS:
>	- store and print many variables
>	- understand importance of good naming conventions and code readability
>	- store similar variables in an **list**(array)
>	- loop through the variables (**for x in xs**) and 'temporary' variables
>	- understand performance implications of improving your code (**2n vs n+1 vs 4 lines of code**)

Let's store some planet information. We'll need a new file:

- create a file in that folder `touch planets.py`
- open that file in atom editor `atom planets.py`

Students: In that new file, create a variable called planet and put in it  string 'Mercury'. Then print it on the screen. You know how to do it!
Students run the file. Make sure they run the correct file.

```python
planet1 = "Mercury"
print(planet1)
```

Students: Now let's store more than one planet. Create two more variables, call them planet1, planet2, etc. Print them all to the screen.

```python
planet1 = "Mercury"
planet2 = "Venus"
planet3 = "Earth"

print(planet1)
print(planet2)
print(planet3)
```

Note that this is all great but if we have 100 planets how many lines of code will we have? (200, as in 100*2) Write that on whiteboard.
But computers are great at storing data. So let's use them for that. We can use something called List, it's a box in which we hold lots of data. It even uses box-looking brackets to do that! (language metaphor: "List of options")

To get things out of a list, you use the INDEX of each item. Think of your index finger - it's for pointing at things - Index in array is a number that points at each item.

```python
planets = [ "Mercury", "Venus", "Earth" ]

print(planets[1])
print(planets[2])
print(planets[3])
```

Oh dear, something is not right. Yes, that's because computers count from 0, not from 1 like humans do. So really we want to say this:

```python
planets = [ "Mercury", "Venus", "Earth" ]

print(planets[0])
print(planets[1])
print(planets[2])
```

Notice that now for 100 planets we would only need 101 lines of code! So we need n + 1. That's a dramatic improvement but still a lot of typing! Let's make this even better.

We can LOOP through the array. That means we can perform some action on each item of it! Notice loop has two elements:

- What are we looping through and how shall we call each element when it's their time `for planet in planets .... end`
- What is the action that should be performed on each loop `print(planet)`

you can think of planet as a temporary variable, that will only exist in the realm of this loop block (train track, in our metaphor). We need to give it a name, so that we can do things to it. You can use a methaphor of teaching a child to read each card in a deck (we'll use that methaphor later again). You would say: "Go through all cards in a deck, one CARD at a time, and each time read THAT CARD".

```python
planets = [ "Mercury", "Venus", "Earth" ]

for planet in planets:
    print(planet)

```

Notice that now how many lines do we need for 100 planets? just 4. How about for a million planets? Also 4. This is very efficient, because we used computer for something they are really good at!

## Ask about a short break here if needed

## **Combining many moving parts**

>  LEARNING GOALS:
>	- combine all your coding knowledge together into a game (**if in a loop**)
>	- experience your first bug (**else in a loop**)
>	- know where the concept of "debugging" comes from
>	- tackle solving a bug by reasoning (how would you explain it to an 8 year old)
>	- know the concept of a boolean flag (**a true/false variable**)
>	- extract user output out of the logic as an example of good coding practice and separation of responsibility
>	- understand that we have build a full stack app (data, input, logic, controller, output)

In the last section we will not learn anything new, but we'll combine all the knowledge we have to create a full stack game. What's full stack? No spoilers! You will find out at the end.

Tell students that if at any points things get too much, they can close their laptops and just watch you code.

Students: Add a few more planets. Then ask user what's their favourite planet. Capture their response in a variable guess and repeat it to them. Then say goodbye.

```python
planets = [ "Mercury", "Venus", "Earth", "Mars" , "Jupiter"]

favourite = input("What's your favourite planet? ")

print(f"You said: {favourite}, thank you")

for planet in planets:
    print(planet)


print("Goodbye!")
```

When we're looping through planets, it's not very useful to just print them all, let's do something else instead.

Students: Print to the screen a message based on whether the favourite planet is in the solar system, or not.
Like "Mars is in solar system" or "Mars is not in solar system".
Students: Use if else, which you know how to use already.

note: students most likely will produce below code, so go along with it and type that on the screen. It will introduce a bug.

```oython
planets = [ "Mercury", "Venus", "Earth", "Mars" , "Jupiter"]
favourite = intput("What's your favourite planet?")
print(f"You said: {favourite}, thank you")

for planet in planets:
  if favourite == planet:
      print(f"{favourite} is in solar system!")
  else
    print(f"{favourite} ISN'T in solar system!")


print("Goodbye!")
```

this produces a bug, because a message is printed too many times, like this:

```
Mars
You said: Mars, thank you
Mars ISN'T in solar system!
Mars ISN'T in solar system!
Mars ISN'T in solar system!
Mars is in solar system!
Mars ISN'T in solar system!
Goodbye!
```

This is not correct, discuss briefly with students if they understand what is going on. You can use the metaphor of the little child going through a list of cards, in search of an Ace of Spades, and shouts "Ace of Spades is not in a deck!" every time she sees a cards that's not an Ace of Spades. Amongst all that oversharing and shouting child might eventually shout "Ace of Spades is in a deck!" if it's in the deck.

What the child should rather do is: go through all the cards and keep in their mind if the card was already found or not. And then at the very end, after seeing all the cards, they can say "Ace of Spades IS / ISN'T  in a deck!"

Fun fact: Unexpected behaviour in a computer program is called a computer Bug, notably because Grace Hopper described a month that got stuck in the insides of their computer and caused it to malfunction. (for interested: It was in the relay, which is sort of like a light switch or a piano key).

## Final part: Full Stack and architecture

> **Depending on time left and on how tired the group is: here likely you will just ask students to close their laptops and watch you code the last part**

>  LEARNING GOALS:
>	- know the concept of a boolean flag (**a true/false variable**)
>	- extract user output out of the logic as an example of good coding practice and separation of responsibility
>	- understand that we have build a full stack app (data, input, logic, controller, output)

Note: at this point depending on the time, you might tell the class to close their laptops and just pay attention to the code you are creating. You can make it quite discursive and indeed explain to them what Mob programming is ("like with pitchforks and torches").

We already know that computers can store a piece of information in a little bucket, called variable. We can store strings, numbers or even arrays. But another thing we can store, and something that computers love is a true/false value (it's basically 0 or 1). We call them Boolean values, from the name of George Boole who popularised the idea.  

- Add a did_i_find_it variable and explain why it would start as a false.
- Cut out the if/else where we print if the planet was found or not
- Then explain how loop through planets can change did_i_find_it to true whenever the planet was found
- finally paste the if/else back, at the end, and change the condition that triggers it to did_i_find_it == true

```python
planets = [ "Mercury", "Venus", "Earth", "Mars" , "Jupiter"]

favourite = input("What's your favourite planet? ")

print(f"You said: {favourite}, thank you")

did_i_find_it = False

for planet in planets:
    if favourite == planet:
        did_i_find_it = True

if did_i_find_it == True:
    print(f"Yay! {favourite} is in Solar System")
else:
    print(f"Sorry, {favourite} is not In Solar System")

print("Goodbye!")
```

Have students play the game a few times.

### Full-stack app and what is software architecture

Explain that this basically concludes the lesson, but you want to bring their attention to the architectural choices that we've made. This simple game follows what we call a Model-View-Controller + Data architecture, and could be described as a full stack app.

**Full Stack** means that you are building everything needed for a successful app. If app was a restaurant, full stack consists of the Front-End and Back-End. Back-end is the kitchen, hobs, ingredients, cooks, the printer through which the orders come in and the window through which the food comes out - everything that the user does not see. Front end will be the chairs, tables, waiters, printed menus, sigh over the entrance - everything that the user does see.

**Front-End** is what user sees and interacts with:

- View (prints) this is things that the user interacts with, what they see and click and type. Notice that right now this is text on the screen, but might just as well be voice on amazon echo, pretty buttons on a website or physical lamp in a spaceship

**Back-End** is everything that the user does not see, but is happening behind the scenes:

- Data storage (planets) which can be written in code (like we did it), or read from a file, or from a database. Notice that if we changed how planets data get in to the array, the rest of the app will still work smoothly.
- Model (boolean flag, for loop and the 'if' inside it) - this is where we extract all the knowledge and decision making of our program. Notice that there might be some improvements we do do the way we search and communicate our findings, but the rest of the app should still work the same if we adjust it.
- Controller (selecting what View to show based on the data). This is the part that connects all the other parts. It can also be swapped, or improved, without impacting on the rest of the system. You can think of how the Amazon website looks different depending on if you are logged in or not. There's probably a boolean flag is_user_logged_in (true or false) in their code. Based on its value Amazon might show you the Log In button or Log Out button.

This was a simplified example of Full Stack MVC+D model, but hopefully you see the modular architecture of code that makes it convenient to work on and error-proof.
