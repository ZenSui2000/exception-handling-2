# exception-handling-2

1.   We need to use custom exception because :
      1.To improve readability of your code.
      2.To enhance reusability of features.
      3.To provide custom messages/instructions to users for specific use cases.


 2.   import inspect

def treeClass(cls, ind = 0):
	print ('-' * ind, cls.__name__)
	
	for i in cls.__subclasses__():
		treeClass(i, ind + 3)

print("Hierarchy for Built-in exceptions is : ")

treeClass(BaseException)


3.    There are three errors defined in arithmetic class 
      OverflowError, ZeroDivisionError, FloatingPointError

  try:
  arithmetic = 5/0
  print(arithmetic)
except ArithmeticError:
  print('You have just made an Arithmetic error')

try:
    1/0
except ArithmeticError as e:
    print(f"{e}, {e.__class__}")



4. Lookup error class is used because LookupError Exception is the Base class for errors raised when something can't be found. 

pylenin_info = {'name': 'Lenin Mishra',
                'age': 28,
                'language': 'Python'}
user_input = input('What do you want to learn about Pylenin==> ')

try:
    print(f'{user_input} is {pylenin_info[user_input]}')
except LookupError as e:
    print(f'{e}, {e.__class__}')



5. ImportError occurs when the Python program tries to import module which does not exist in the private table.
The 'module not found' error is a syntax error that appears when the static import statement cannot find the file at the declared path.


6. Some best practices in python exception handling are :
    
Use Exceptions for Exceptional Cases. ...
Don't Swallow the Exception. ...
Catch Specific Exceptions. ...
Always Clean Up Resources in a Finally Block. ...
Avoid Raising Generic Exceptions. ...
Raise Custom Exceptions. ...
Define Your Own Exception Hierarchy. ...
Document All Exceptions Thrown by a Function.
