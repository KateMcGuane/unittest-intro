## Function Pseudo Code
- Write a function that accepts a list of numbers and returns true if the list contains an even number of even numbers.
- Should raise a TypeError if anything other than a list is passed into the function.


## Suggestested Tests
    1. Should raise a TypeError if a list is not passed into the function.
    2. If numbers is empty, return False
    3. If the number of even numbers is odd, return False
    4. If the number of even numbers is 0, return False
    5. If the number of even numbers is even, return True


## Notes

### Python
- When Python runs a file directly, it names it __main__ and any code beneath the if statement will only be run if the name of the file is __main__.
So when we run the test file it will have the name __main__ and this code won't run.  
But when we run this file it will have the name __main__ and it will run this code.


### Unittest 
- Unittest requires that our test  filename starts with the word ‘test’,  
followed by an underscore and a  descriptive name of what we’re testing.
- Does not need installation as it is part of the standard Python library.
- Adding a pass statement to our class allows us to run the file without specifying the unit test module.
- Pass statement allows us to run the code error free --> for when you have no code to run but allows it to pass as valid


## Steps

### Set Up
- Import the Unittest  module: 'import unittest' to test_file
- Create test case -- via a class that passes unittest in as an argument
- Write initial function
- Import file with code into test_file


### Building a function using TDD - Red & Green
-  Add a check in our function  that checks if the value passed in is a list, and if it is, return True else raise a TypeError.
- Test should test our function returns False if an empty list is passed in
- Test for two even numbers --> would want it to pass
- Create fail test for if only one even number is passed in
- Need to  count the number of even numbers in the list and then check if that number itself is even
- Create assert that adds odd number of odd numbers --> should be returning True when it is returning False (a True fail should return False)
- Use a truthy falsy value check of evens, so if evens is > 0 it will evaluate to True and False if it is 0 And within the if evens is greater than 0,  
we can return evens % 2 == 0.


### Refactor - DRY (Don't Repeat Yourself)