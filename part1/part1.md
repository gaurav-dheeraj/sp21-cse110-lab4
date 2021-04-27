# Part 1

## Part 1a

1. values added:  20
2. final result:  20
3. values added:  20
4. This returns an error (ReferenceError: result is not defined) since result is declared using let and hence, it's scope is limited to the if block. It cannot be accessed in line 13.
5.  "TypeError: Assignment to constant variable" is the error returned in line 7 due to result, which is declared as a const, being reassigned. So, line 9 would not print anything.
6.  "TypeError: Assignment to constant variable" is the error returned in line 7 due to result, which is declared as a const, being reassigned. So, line 13 would not print anything.


## Part 1b

1. This logs a value of 3 to the console. This is because the value of i at the line 12 would be the value after the for loop terminates and this happens when i = prices.length = 3. i can be accessed outside the for loop as it is declared using var.
2. This logs a value of 150 to the console. This is because the value of discountedPrice at the line 13 would be the value after the for loop terminates and it would have the value 150 as the last time discountedPrice is updated when i=2. discountedPrice = prices[2] * (1 - discount) = 300 * (1 - 0.5) = 150. discountedPrice can be accessed outside the for loop as it is declared using var.
3. This logs a value of 150 to the console. This is because the value of finalPrice at the line 14 would be the value after the for loop terminates and it would have the value 150 as the last time lastPrice is updated when discountedPrice=150 as explained in the prvious answer. finalPrice is within the scope for line 14 but as it's declared with var, it has global scope. finalPrice = Math.round(discountedPrice * 100) / 100 = Math.round(150 * 100) / 100 = 150.
4. Returns the array of the final prices [ 50, 100, 150 ] and discounted is within the scope for line 16 (where the return statement is) but as it's declared with var, it has global scope. The elements in discounted array are the final discounted prices of the respective elements in the prices array and after doing the respective calculations in the for loop, they are pushed accordingly to discounted array.
5. This gives a ReferenceError: i is not defined because i is confined to the for construct and cannot be accessed at line 12.
6. This gives a ReferenceError: discountedPrice is not defined because discountedPrice is confined to the for construct and cannot be accessed at line 13.
7. Prints 150 due to calculations similar to Q3. finalPrice is within the scope for line 14 as it is declared outside the for loop within the same function. 
8.  Returns the array of the final prices [ 50, 100, 150 ] and discounted is within the scope for line 16 as it is declared outside the for loop within the same function. 
9. This gives a error (ReferenceError: i is not defined) because i is declared using let and is hence confined to the for construct. i cannot be accessed at line 11.
10. Prints 3 becuase there is no reassignment or redeclaration of length after being declared as a const and is declared in the same function outside the for loop as line 12. It holds the value 3 as it is the length of the prices array.
11. Returns the array of the final prices [ 50, 100, 150 ] and discounted is declared in the same function outside the for loop as line 14. It allows us to push values to a const array as we are not reassigning or redeclaring discounted and hence we're able to get the respective discounted values for the elements in prices in the discounted array even though it is declared as a const.
12. A. student.name
    B. student['Grad Year']
    C. student.greeting()
    D. student["Favorite Teacher"].name
    E. student.courseLoad[1]
13. A. '32' - since integers map to their exact string representation and string concatenation is done when the + sign is used with a string and integer.    
    B. 1 - returns a number type since '-' represents an arithmetic subtraction and the string is converted to its exact integer representation.  
    C. 3 - returns a number type as '+' used with a number and null represents an arithmetic addition and null is converted to the integer representation of 0.  
    D. '3null' - here, the '+' represents a concatenation and null is converted to "null".  
    E. 4 - returns a number type as '+' used with a number and boolean represents an arithmetic addition and true is converted to the integer representation of 1.  
    F. 0 - returns a number type as '+' represents an arithmetic addition and both false and null are converted to the number representation of 0.  
    G. '3undefined' - here, the '+' represents a concatenation and undefined is converted to 'undefined'.  
    H. NaN - because '-' represents an arithmetic subtraction and undefined is converted to NaN and any operation on NaN returns an NaN.  

14. A. true - since '2' is converted to its exact integer representation and it is indeed greater than 1.  
    B. false - the ASCII values of the first characters in both strings are compared and the ASCII value of 2 is not lower than 1.  
    C. true - The regular equality check is done. '2' is converted to 2 and is indeed equal to 2.  
    D. false - The strict equality check is done. Since '2' is a string and 2 is a number, the data types differ and the strict equality returns false.  
    E. false - When comparing values of different types, JavaScript converts the values to numbers. true is converted to 1 and is hence not equal to 2.  
    F. true - Strict equality check is done. Boolean(2) is converted to true and is of the same type (boolean) and value as true.  

15. == is a regular equality check where if different data types are compared, they are first converted to numbers and then compared. So, even if they are different data types, as long as they map to the same number representation, == returns true.  
    === is a strict equality check where no data type conversion is done. Both operands must be of the same data type and must have the same value for it to return true.
16. Present in the file part1b-question16.js
17. [ 2, 4, 6 ] will be returned by modifyArray([1,2,3], doSomething). This is because doSomething is used as a callback which is called whenever the loop is iterated. The array [1, 2, 3] is traversed through by the loop and doSomething() is called for each element in this array. The respective number is doubled in doSomething() and this value is pushed to the array that is returned after the loop is terminated.
18. Present in the file part1b-question18.js
19. 1  
    4  
    3  
    2