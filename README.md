# Python-Primer
 
#NOTE: each question is separated by a space

#print name
print("Alexandra Burkeen")

#print song lyrics
print("I am machine, I never sleep")
print("Until I fix what's broken")
print("I am machine, a part of me")
print("Wishes I can just feel something")

#make a program that displays several numbers
print(1)
print(2)
print(3)
print(4)

#make a program that solves and shows the summation of 64+32
print(59+24)

#do  the same as above, but sum x + y
x = 20
y = 5
print(x+y)

#make program that displays favorite actor
print("Johnny Depp")

#print lucky inside s
s = "I am lucky"
print(s[5:10])

#print current day
s = "Today is %d/%d/%d" % (3,15,2021)

#test string replace
oldstring = "no yes no yes no"
print(oldstring.replace("yes", "no",3))

#is string.find() case sensitive?
find = "I i aye"
print(find.find("i"))
#yes, .find() is case sensitive, because index 2 is returned instead of index 0

#what if occurence appears twice in string?
find2 = "I i i aye"
print(find2.find("i"))
#the first element is displayed 

#Write a program that asks console input and searches for a query.
value = input("enter a string to be checked:")
print(value.find("are"))

#Create a list of words and join them, like the example above.
word1 = "right"
word2 = "as"
word3 = "rain"
print(f'{word1} {word2} {word3}')

#Try changing the separator string from a space to an underscore.
str = "Hello World"
print(str.replace(" ", "_"))

#Can a string be split on multiple characters?
#yes, a string can be split on mult chars
string = "Barry is a cat"
print(string.split("is"))

#Can you split a string this string?: World,Earth,America,Canada
places = "World,Earth,America,Canada"
print(places.split(","))

#Given an article, can you split it based on phrases?
#Yes, you could use article.split("phrase")

#Make a program that creates a random number and stores it into x.
import random
x = random.randint(0,1000)
print(x)

#Make a program that prints 3 random numbers.
print(random.randint(0,10000),random.randint(0,10000),random.randint(0,10000))

#Create a program that generates 100 random numbers and find the frequency of each number
listRand = []
for a in range(100):
  listRand.append(random.randint(1,20))
#Count the number of occurrences 
def countNum(lst, x): 
    count = 0
    for elem in lst: 
        if (elem == x): 
            count = count + 1
    return count 
#call function from above for 1-10
for x in range(20):
  print('{} has occurred {} times'.format(x, countNum(listRand, x))) 

#Make a program that asks a phone number.
phone = input("Please enter your phone number:")
lang = input("Please enter your preferred programming language:")

# *** PROS AND CONS OF PYTHON *** 
#pros: good for data analysis, lots of good import packages, very easy to use
#cons: slow, weak for mobile computing, unique syntax

#Make a program that asks the number between 1 and 10. If the number is out of range the program should display “invalid number”.
input1 = int(input("Please enter a value between 1-10:"))
if 1 <= input1 <= 10:
  print("Valid number")
else:
  print("Invalid number")

#Make a program that asks a password.
password = input("Please enter the password:")
if password == "thisPassword":
  print("Password correct!")
else:
  ("Password incorrect...")

"""
1. Make a program that lists the countries in the set
clist = ['Canada','USA','Mexico','Australia']
2. Create a loop that counts from 0 to 100
3. Make a multiplication table using a loop
4. Output the numbers 1 to 10 backwards using a loop
5. Create a loop that counts all even numbers to 10
6. Create a loop that sums the numbers from 100 to 200
"""
#1
clist = ['Canada','USA','Mexico','Australia']
for n in clist:
  print(n)
#2 
for i in range(100):
  print(i)
#3
for multi1 in range(6): 
  for multi2 in range(6):
    print((multi1 + 1)*(multi2 + 1))
#4
for i in range(10):
  print(10-i)
#5
for i in range(10):
  if (i % 2 == 0):
    x++
print(x)
#6
sum1 = 0
for i in range(100):
  sum1 += (i+100)
print(sum1)

"""
1. Make a program that lists the countries in the set below using a while loop.
clist = ["Canada","USA","Mexico"]
2. What‟s the difference between a while loop and a for loop?
3. Can you sum numbers in a while loop?
4. Can a for loop be used inside a while loop?
"""
#1
clist = ["Canada","USA","Mexico"]
i = 0
while i < len(clist):
  print(clist[i])
  i += 1
#2
#for loop will run for a set amount of iterations.
#while loop will run until condition turns false. 
#3
#Yes, you can sum numbers within a while loop.
#4
#Yes, a for loop can be used inside of a while loop.

"""
1. Make a function that sums the list mylist = [1,2,3,4,5]
2. Can functions be called inside a function?
3. Can a function call itself? (hint: recursion)
4. Can variables defined in a function be used in another function? (hint: scope)
"""
#1
def sum_list(list1):
  sum1 = 0
  for i in range(len(list1)):
    sum1 += (list1[i])
  print(sum1)
list1 = [1,2,3,4,5]
sum_list(list1)
#2
#Yes, functions can be called inside of another function.
#3
#Yes, function can call another function.
#4 
#Variables in a function can be used in another function only if they are returned.

"""
Make a program that displays the states in the U.S.
states = [ 'Alabama', .. ,'Wyoming' ]
Display all states starting with the letter M
"""
states = [ 'Alabama', 'Montana', 'Michigan', 'Idaho', 'Utah', 'Mississippi' ]
for i in range(len(states)):
  if states[i][0] == 'M':
    print(states[i])

#Given the list y = [6,4,2] add the items 12, 8 and 4.
y = [6,4,2]
y.extend([12,8,4])
print(y)
#Change the 2nd item of the list to 3.
y[1] = 3
print(y)

#Given a list with pairs, sort on the first element
# take first element for sort
def takeFirst(elem):
    return elem[0]
x = [ (3,6),(4,7),(5,9),(8,4),(3,1)]
x.sort(key=takeFirst)
print(x)

#Now sort on the second element
# take second element for sort
def takeSecond(elem):
    return elem[1]
x = [ (3,6),(4,7),(5,9),(8,4),(3,1)]
x.sort(key=takeSecond)
print(x)

#Create a list of one thousand numbers
my_list = list(range(1, 1001))
#Get the largest and smallest number from that list
print(min(my_list))
print(max(my_list))
#create two lists, an even and odd one.
oddList = []
evenList = []
for i in range(len(my_list)):
  if my_list[i] % 2 == 0:
    evenList.append(my_list[i])
  else:
    oddList.append(my_list[i])
print(evenList)
print(oddList)

#Make a mapping from countries to country short codes
countries = {'United States' : 'US', 'Australia' : 'AU', 'Spain' : 'ES'}
#Print each item (key and value)
for i in countries:
  print(i, countries[i])

#Read a file and number every line
#f = open("demoFile.txt", "r")
#f.read() 
#Find out what the program does if the file doesn't exist.
#Error message: file not accessible
#What happens if you create a file with another user and try to open it?
#You will be unable to open it

#Write the text “Take it easy” to a file
#f.write('Take it easy')
#Write the line open(“text.txt”) to a file
#f.write("open(“text.txt”)")

#Given a tic-tac-toe board of 3x3, print every position
for i in range(3):
  for j in range(3):
    print(i,j)
#Create a program where every person meets the other
persons = ["John", "Henry", "Peter", "Josh", "Mary", "Joanna"]
for i in range(len(persons)):
  j = i
  while j < len(persons) -1:
    print(f"{persons[i]} meets {persons[j+1]}") 
    j += 1
#If a normal for loop finishes in n steps O(n), how many steps has a nested loop?
#O(n^2)

#Take a slice of the list below:
pizzas = ["Hawaii","Pepperoni","Fromaggi","Napolitana","Diavoli"]
print(pizzas[2:4])
#Given the text “Hello World”, take the slice “World”
string = "Hello World"
print(string[6:11])

#Create a function that returns a,b and a+b
def func1(a,b):
  sum1 = a+b
  list1 = [a,b]
  return list1, sum1

print(func1(1,3))

#Create a function that returns 5 variables
def five_var(a,b):
  one = a * b
  two = one * 2
  three = one * 3
  four = one * 4
  five = one * 5
  return one,two,three,four,five
print(five_var(2,3))

#Add a function reduce amount that changes the variable balance
#Create a function with a local variable
def reduce_balance(balance):
  new_bal = balance - 100
  return new_bal
initial_balance = 1000
new_balance = reduce_balance(initial_balance)

#Print the date in format year-month-day
from datetime import date
today = date.today()
print("Today's date:", today)

#Can try-except be used to catch invalid keyboard input?
#Yes
#Can try-except catch the error if a file can‟t be opened?
#Yes
#When would you not use try-except?
#When dealing with errors(ex: out of memory)

#Can you have more than one class in a file?
#Yes
#Can multiple objects be created from the same class?
#Yes
#Can objects create classes?
#No, objects are instances of classes

#Using the code above, create another object?
class Person:
    "This is a person class"
    #getter method 
    def getAge(self): 
        return self._age 
      
    #setter method 
    def setAge(self, x): 
        self._age = x 

    def greet(self):
        print('Hello hello!')

Allie = Person()
#Add a method to the class: location()
def location(self):
      print("Pennsylvania")

#Add a variable age and create a getter and setter 
Allie.setAge(24)  
print(Allie.getAge()) 

#Why would you use getter and setter methods?
#Ensures data encapsulation, which avoids direct access to a specific variable 

#Import the math module and call the sin function
import math
print(math.sin(6))

#Create your own module with the function snake()
def snake():
  print("I am a snake. I have no legs. Do not touch me! I will bite you.")
#file is main.py
import main
main.snake()

#Create a new class that inherits from the class App
#class parent_class_name extends App - class header
#Try to create a class that inherits from two super classes (multiple inheritance)
class Base1:
    pass

class Base2:
    pass

class MultiClass(Base1, Base2):
    pass

#Can a method inside a class be called without creating an object?
#Yes - this is called a static method
#Why does not everybody like static methods?
#Static methods have limited use, because they don't have access to the attributes of an instance of a class, and they don't have access to the attributes of the class itself. Its not the best for long-term use.

#What is an iterable?
#An iteratable is a Python object that can be used as a sequence. You can go to the next item of the sequence using the next() method. It’s a container object: it can only return one of its element at the time. 
#Which types of data can be used with an iterable?
#Examples of iterables include all sequence types (such as list , str , and tuple ) and some non-sequence types like dict , file objects, and objects of any classes you define with an __iter__() method or with a __getitem__() method that implements Sequence semantics

#What is a classmethod?
#A class method is a method that’s shared among all objects. Class methods can be can be called from instances and from the class itself
#How does a classmethod differ from a staticmethod?
#static method is not bound to any one class, while a class method is

#Do all programming languages support multiple inheritance?
#No 
#Why would you not use multiple inheritance?
#To prevent ambiguity
#Is there a limit to the number of classes you can inherit from?
#No
