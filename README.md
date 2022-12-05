Q.1. What are the key features of Python?

If it makes for an introductory language to programming, Python must mean something. These are its qualities:

Interpreted
Dynamically-typed
Object-oriented
Concise and simple
Free
Has a large community

Q.2. Differentiate between lists and tuples.

The major difference is that a list is mutable, but a tuple is immutable. Examples:

>>> mylist=[1,3,3]
>>> mylist[1]=2
>>> mytuple=(1,3,3)
>>> mytuple[1]=2
Traceback (most recent call last):

File “<pyshell#97>”, line 1, in <module>

mytuple[1]=2

TypeError: ‘tuple’ object does not support item assignment

Python Tuples vs Lists – A Detailed Comparison

Q.3. Explain the ternary operator in Python.

Unlike C++, we don’t have ?: in Python, but we have this:

[on true] if [expression] else [on false]

If the expression is True, the statement under [on true] is executed. Else, that under [on false] is executed.


Below is how you would use it:

>>> a,b=2,3
>>> min=a if a<b else b
>>> min
2

>>> print("Hi") if a<b else print("Bye")
Hi

Q.4. What are negative indices?

Let’s take a list for this.

>>> mylist=[0,1,2,3,4,5,6,7,8]
A negative index, unlike a positive one, begins searching from the right.

>>> mylist[-3]
6

This also helps with slicing from the back:

>>> mylist[-6:-1]
[3, 4, 5, 6, 7]

Q.5. Is Python case-sensitive?

A language is case-sensitive if it distinguishes between identifiers like myname and Myname. In other words, it cares about case- lowercase or uppercase. Let’s try this with Python.

>>> myname='Ayushi'
>>> Myname
Traceback (most recent call last):

File “<pyshell#3>”, line 1, in <module>

Myname

NameError: name ‘Myname’ is not defined

As you can see, this raised a NameError. This means that Python is indeed case-sensitive.


Q.6. How long can an identifier be in Python?

According to the official Python documentation, an identifier can be of any length. However, PEP 8 suggests that you should limit all lines to a maximum of 79 characters. Also, PEP 20 says ‘readability counts’. So, a very long identifier will violate PEP-8 and PEP-20.

Apart from that, there are certain rules we must follow to name one:

It can only begin with an underscore or a character from A-Z or a-z.
The rest of it can contain anything from the following: A-Z/a-z/_/0-9.
Python is case-sensitive, as we discussed in the previous question.
Keywords cannot be used as identifiers. Python has the following keywords:
and	def	False	import	not	True
as	del	finally	in	or	try
assert	elif	for	is	pass	while
break	else	from	lambda	print	with
class	except	global	None	raise	yield
continue	exec	if	nonlocal	return
Learn everything about Python Identifiers

Q.7. How would you convert a string into lowercase?

We use the lower() method for this.

>>> 'AyuShi'.lower()
‘ayushi’

To convert it into uppercase, then, we use upper().

>>> 'AyuShi'.upper()
‘AYUSHI’

Also, to check if a string is in all uppercase or all lowercase, we use the methods isupper() and islower().

>>> 'AyuShi'.isupper()
False


>>> 'AYUSHI'.isupper()
True

>>> 'ayushi'.islower()
True

>>> '@yu$hi'.islower()
True

>>> '@YU$HI'.isupper()
True

So, characters like @ and $ will suffice for both cases

Also, istitle() will tell us if a string is in title case.

>>> 'The Corpse Bride'.istitle()
True

Q.8. What is the pass statement in Python?

There may be times in our code when we haven’t decided what to do yet, but we must type something for it to be syntactically correct. In such a case, we use the pass statement.

>>> def func(*args):
pass
>>>
Similarly, the break statement breaks out of a loop.

>>> for i in range(7):
if i==3: break
print(i)
1

2

Finally, the continue statement skips to the next iteration.

>>> for i in range(7):
if i==3: continue
print(i)

1

2

4

5

6

Hope you have read all the basic Python Interview Questions and Answers. Now, let’s move towards the second part of the blog – Most asked Python Interview Questions and Answers for freshers

Frequently Asked Python Interview Questions and Answers for Freshers
While solving or answering these questions, if you feel any difficulty, comment us. DataFlair is always ready to help you.

Q.9. Explain help() and dir() functions in Python.

The help() function displays the documentation string and help for its argument.

>>> import copy
>>> help(copy.copy)
Help on function copy in module copy:

copy(x)

Shallow copy operation on arbitrary Python objects.

See the module’s __doc__ string for more info.

The dir() function displays all the members of an object(any kind).

>>> dir(copy.copy)
[‘__annotations__’, ‘__call__’, ‘__class__’, ‘__closure__’, ‘__code__’, ‘__defaults__’, ‘__delattr__’, ‘__dict__’, ‘__dir__’, ‘__doc__’, ‘__eq__’, ‘__format__’, ‘__ge__’, ‘__get__’, ‘__getattribute__’, ‘__globals__’, ‘__gt__’, ‘__hash__’, ‘__init__’, ‘__init_subclass__’, ‘__kwdefaults__’, ‘__le__’, ‘__lt__’, ‘__module__’, ‘__name__’, ‘__ne__’, ‘__new__’, ‘__qualname__’, ‘__reduce__’, ‘__reduce_ex__’, ‘__repr__’, ‘__setattr__’, ‘__sizeof__’, ‘__str__’, ‘__subclasshook__’]

Q.10. How do you get a list of all the keys in a dictionary?


Be specific in these type of Python Interview Questions and Answers.

For this, we use the function keys().

>>> mydict={'a':1,'b':2,'c':3,'e':5}
>>> mydict.keys()
dict_keys([‘a’, ‘b’, ‘c’, ‘e’])

Wait!! Have you developed any Python Project yet?

Practice with Top Python Projects with source code and become job-ready

Q.11. What is slicing?

Slicing is a technique that allows us to retrieve only a part of a list, tuple, or string. For this, we use the slicing operator [].

>>> (1,2,3,4,5)[2:4]
(3, 4)

>>> [7,6,8,5,9][2:]
[8, 5, 9]

>>> 'Hello'[:-1]
‘Hell’

Q.12. How would you declare a comment in Python?

Unlike languages like C++, Python does not have multiline comments. All it has is octothorpe (#). Anything following a hash is considered a comment, and the interpreter ignores it.

>>> #line 1 of comment
>>> #line 2 of comment
In fact, you can place a comment anywhere in your code. You can use it to explain your code.

Q.13. How will you check if all characters in a string are alphanumeric?

For this, we use the method isalnum().


Q.14. How will you capitalize the first letter of a string?

Simply using the method capitalize().

>>> 'ayushi'.capitalize()
‘Ayushi’

>>> type(str.capitalize)
<class ‘method_descriptor’>

However, it will let other characters be.

>>> '@yushi'.capitalize()
‘@yushi’

>>> 'Ayushi123'.isalnum()
True

>>> 'Ayushi123!'.isalnum()
False

Other methods that we have include:

>>> '123.3'.isdigit()
False

>>> '123'.isnumeric()
True

>>> 'ayushi'.islower()
True

>>> 'Ayushi'.isupper()
False

>>> 'Ayushi'.istitle()
True


>>> ' '.isspace()
True

>>> '123F'.isdecimal()
False

Q.15. We know Python is all the rage these days. But to be truly accepting of a great technology, you must know its pitfalls as well. Would you like to talk about this?

Of course. To be truly yourself, you must be accepting of your flaws. Only then can you move forward to work on them. Python has its flaws too:

Python Interview Question - limitations of Python

Python’s interpreted nature imposes a speed penalty on it.
While Python is great for a lot of things, it is weak in mobile computing, and in browsers.
Being dynamically-typed, Python uses duck-typing (If it looks like a duck, it must be a duck). This can raise runtime errors.
Python has underdeveloped database access layers. This renders it a less-than-perfect choice for huge database applications.
And then, well, of course. Being easy makes it addictive. Once a Python-coder, always a Python coder.
Q.16. With Python, how do you find out which directory you are currently in?


To find this, we use the function/method getcwd(). We import it from the module os.

>>> import os
>>> os.getcwd()
‘C:\\Users\\lifei\\AppData\\Local\\Programs\\Python\\Python36-32’

>>> type(os.getcwd)
<class ‘builtin_function_or_method’>

We can also change the current working directory with chdir().

>>> os.chdir('C:\\Users\\lifei\\Desktop')
>>> os.getcwd()
‘C:\\Users\\lifei\\Desktop’

Q.17. How do you insert an object at a given index in Python?

Let’s build a list first.

>>> a=[1,2,4]
Now, we use the method insert. The first argument is the index at which to insert, the second is the value to insert.

>>> a.insert(2,3)
>>> a
[1, 2, 3, 4]

Q.18. And how do you reverse a list?

Using the reverse() method.

>>> a.reverse()
>>> a
[4, 3, 2, 1]

You can also do it via slicing from right to left:

>>> a[::-1]
>>> a
[1, 2, 3, 4]


This gives us the original list because we already reversed it once. However, this does not modify the original list to reverse it.

Q.19. What is the Python interpreter prompt?

This is the following sign for Python Interpreter:

>>>
If you have worked with the IDLE, you will see this prompt.

Q.20. How does a function return values?

A function uses the ‘return’ keyword to return a value. Take a look:

>>> def add(a,b):
return a+b
