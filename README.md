# Ruby 2: Recap and Methods

## Objective

Students get a review of the core concepts learned in the earlier lesson, puts, strings, math, and user input. Students get introduced to methods.

## SWBAT

+ METHODS - Define a method in ruby.
+ METHODS - Call a method in ruby.

## Recap

Feel free to use [Ruby Recap and Methods Deck](https://docs.google.com/presentation/d/1zOL_KZKVK-jW8Gyh5L-XPgHw8XXkZytKWb7W4SqDKP0/edit#slide=id.g38c2de6ae8_0_122)

+ Programs are Just Files

+ Strings Review

+ Reading Errors Review

#### CFU 

Define puts and strings with an elbow partner. Share whole group.

## Methods

In order to not repeat ourselves all the time, we can grab a sequence of commands and put them inside of a method. The method's name becomes a reference to all those commands and every time we call that method, the code inside of it will run.

Have students open `irb` and play with some method definitions

Display the following as an example:

```ruby
def about_me
  puts "My name is Karlie"
  puts "I grew up in St. Louis"
  puts "I'm 25 Years Old"
  puts "My favorite food is Kookies"
end
```

Just defining a method does nothing, it only creates the method. When we want to run it, we have to call it by the name we gave it.

Students can write a practice `about_me` on white boards along with instructors. (Can replace Karlie and her information with your own.)

```ruby
def about_me
  puts "My name is Karlie"
  puts "I grew up in St. Louis"
  puts "I'm 25 Years Old"
  puts "My favorite food is Kookies"
end

about_me
#> My Name is Karlie
#> I grew up in St. Louis
#> I'm 25 Years Old
#> My favorite food is Kookies
```
#### CFU

Stop & Jot: What is a method? How do I call a method?

**Students should all build an `about_me` method.**

Share: Take a second to learn all about your neighbor from the output on their screen.

**Students should work on [Dance Instructions Lab]<!-- (https://github.com/learn-co-curriculum/kwk-l1-dance-instructions) -->** 15 minutes 
(Objective: SWBAT use def to create a method that prints the steps for a dance of their choosing.)

## Loop Intro

We've learned about building programs, giving commands, strings, math, variables, and methods.

Let's look at tips and tricks of optimizing our methods in IRB. **Students can follow along.**

```ruby
def two_step
  puts "Step to the left."
  puts "Step to the right."
end

two_step
two_step
two_step
```
#### CFU

What do you expect this method to do? (Have students stand and physically run the method.)

How would we tell the two_step to just keep on going, to never stop, just keep on repeating? _Do the dance, it never stops_ (We're leading toward loops). When you hear the word loop, what comes to mind?

## Variable Intro

Let's take a look at this example. **Students should follow along.**

```ruby
def greeting
  puts "Hi Jane, I'm Karlie, how's your afternoon?"
end

greeting
```

What if I want to ask a different friend a question? How about a different time of day? 
In that greeting, we have 3 or 4 things that could be replaced with variables. If we wanted our `greeting` method to be really flexible, we might think of the greeting string as really being:

`local_greeting your_name, I'm my_name, how's your time_of_day?`

**Ask students for a variety of greetings, names and times of day.**

`local_greeting` might be "What's up", or "Hey", or "Yo", or "Konichiwa"

`your_name` might be "Ashley" or "Shannon"

`my_name` might be "Sara Beth" or "Chen"

`time_of_day` might be "morning" or "night" or "afternoon"

We might be able to use variables for this, let's try it, in IRB, students following along. Don't hit enter yet!

```ruby
local_greeting = "Howdy"
your_name = "Archie"
my_name = "Veronica"
time_of_day = "evening"

# The goal being to get a greeting of:
#> "Howdy Archie, I'm Veronica, how's your evening?"

def greeting
  puts "#{local_greeting} #{your_name}, I'm #{my_name}, how's your #{time_of_day}?"
end
```

**What should happen? The variables are defined, the method is defined, as long as the method can read those variables, everything should be fine, right?**

Let's try it by hitting enter.

```ruby
local_greeting = "Howdy"
your_name = "Archie"
my_name = "Veronica"
time_of_day = "evening"

# The goal being to get a greeting of:
#> "Howdy Archie, I'm Veronica, how's your evening?"

def greeting
  puts "#{local_greeting} #{your_name}, I'm #{my_name}, how's your #{time_of_day}?"
end

greeting 
```

The program gives an error.

```
Undefined local variable or method `local_greeting` in `greeting`.
```

Computers never lie, if it says it can't find the variable, it can't find it. So something is missing. We'll cover this tomorrow, get excited!!! (Leading toward arguments).
