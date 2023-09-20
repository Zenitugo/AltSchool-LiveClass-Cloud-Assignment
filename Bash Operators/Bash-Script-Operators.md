## Bash operators are special symbols or characters used in Bash scripting to carry out various operations on values and variables; these operators are frequently employed with commands to carry out numerous operations, comparisons, and conditional checks.

Bash operators include:

## 1. Arithmetic Operators:
**There are seven arithmetic operators which includes addition, subtraction, multiplication, division, modulus, increamental and decremental.**

- **Addition `(+)`** : This operator is used to add two operands or concatenate two strings and returns the result of that operation.
```
num1=20
num2=5
echo $(( num1 + num2 ))
echo $(( 20 + 5 ))
echo $(( 25 ))
```
**output**: 25

- **Subtraction `(-)`** : This operator is used to subtract one operand from the other and returns the result of that operation.
```
num1=20
num2=5

echo $(( num1 - num2 ))
echo $(( 20 - 5 ))
echo $(( 15 ))
```
**output**: 15

- **Multiplication `(*)`** : This operator is used to multiply two operands and returns the result of that operation.
```
num1=20
num2=5

echo $(( num1 * num2 ))
echo $(( 20 * 5 ))
echo $(( 100 ))
```
**output**: 100

- **Division `(/)`** : This operator divides a number by another and returns only its integer part (whole numbers).
```
num1=20
num2=3

echo $(( num1 / num2 ))
echo $(( 20 / 3 ))
echo $(( 6 ))
```
**output**: 6

- **Modulus `(%)`** : This operator divides a  number by another and returns the remainder part (fraction/decimal)
```
num1=20
num2=3

echo $(( num1 % num2 ))
echo $(( 20 % 3 ))
echo $(( 2 ))
```

**output**: 2

- **Incremental operator `(++)`** : This is a unary operator used to increase the operand by one.
```
num1=20
num2=5

sum=$num1+$num2
echo $(( ++sum ))
```
**output**: 26

- **Decremental operator `(++)`** : This is a unary operator used to decrease the operand by one.
```
num1=20
num2=5

sum=$num1*$num2
echo $(( --sum ))
```
**output**: 99

## 2. Logical Operators:
**The logical operators are used for comparing two values or expressions, if they are true then it will return `True` else `False`. These operators are:**

- **Logical And `(&&)`**: This operator returns `true` if both the operands are true otherwise returns `false`.
```
var=40

if [ "$var" -gt 20 -a "$var" -lt 60 ]
then
    echo true
else
    echo false
fi 

Alternatively it can be written in the following ways:

if ["$var" -gt 20] && ["$var" -lt 60]
then
    echo true
else
    echo false
fi

or this way;
if [[ "$var" -gt 20 && "$var" -lt 60 ]]
then
    echo true
else
    echo false
fi
```
**output**: True

- **Logical Or `(||)`** : This operator returns `true` if either of the operands is true or both the operands are true and returns false if none of them is `false`.
```
var=40

if [ "$var" -gt 60 -o "$var" -lt 50 ]
then
    echo true
else
    echo false
fi 

Alternatively it can be written in the following ways:

if [ "$var" -gt 60 ] || [ "$var" -lt 50 ]
then
    echo true
else
    echo false
fi

or this way;
if [[ "$var" -gt 60 || "$var" -lt 50 ]]
then
    echo true
else
    echo false
fi
```
**output**: True

- **Logical Not `(!)`** : This unary operator returns `true` if the operand is false and returns `false` if the operand is true.
```
var=40

if [ ! "$var" -gt 60 -o "$var" -lt 50 ]
then
    echo true
else
    echo false
fi 

Alternatively it can be written in the following ways:
if [[ ! "$var" -gt 60 && "$var" -lt 50 ]]
then
    echo true
else
    echo false
fi
```
**output**: False

## 3. Relational Operators:
**These operators specify the relationship between two operands. Depending on the relationship, they either yield true or false. These operators are:**

- **Equal to `(==)` or `(-eq)`**: It returns `true` if the two operands are equal otherwise returns `false`.
```
var1=40
var2=40

if [[ $var1 -eq $var2 ]]
then
    echo True
else
    echo False
fi
```
**output**: True

- **Not Equal to `(!=)` or `(-ne)`**: It returns `true` if the two operands are not equal otherwise returns `false`.
```
var1=40
var2=20

if [[ $var1 -ne $var2 ]]
then
    echo True
else
    echo False
fi
```
**output**: True

- **Greater than `(>)`or `(-gt)`**: It returns `true` if the first operand is greater than the second operand, otherwise it will return `false``
```
var1=40
var2=20

if [[ $var1 -gt $var2 ]]
then
    echo True
else
    echo False
fi
```
**output**: True

- **Less than `(<)` or `(-lt)`**: The operator returns `true` if the first operand is less than the second operand otherwise returns `false`.
```
var1=40
var2=20

if [[ $var1 -lt $var2 ]]
then
    echo True
else
    echo False
fi
```
**output**: False

- **Less or equal to `(<=)` or `(-le)`**: This operator returns `true` if the first operand is less than or equal to the second operand otherwise returns `false`.
```
var1=40
var2=20

if [[ "$var1" -le "$var2" ]]
then
    echo True
else
    echo False
fi

Another way to write this is:
if (( "$var1" <= "$var2" ))
then
    echo True
else
    echo False
fi
```
**output**: False

- **Greater or equal to `(<=)` or `(le)`** : This operator returns `true` if the first operand is less than or equal to the second operand otherwise returns `false`.
```
var1=40
var2=20

if [[ "$var1" -ge "$var2" ]]
then
    echo True
else
    echo False
fi

Another way to write this is:
if (( "$var1" >= "$var2" ))
then
    echo True
else
    echo False
fi
```
**output**: True
## 4. File Operators:
**In Bash, file operators are used to verify and test files and directories in a variety of ways. In order to show whether a certain condition is satisfied, file operators return a Boolean value (true or false).**

- **b operator**: This operator determines whether or not a file is a block special file. If the file is a block special file, it returns true; otherwise, it returns false.

- **c operator**: This operator determines whether or not a file is a character special file. If the file is a character special file, it returns true; otherwise, it returns false.

The syntax to use any of the file operators is:

```
if [ fileoperator file-name ]

var=/etc/ssh/sshd_config
if [ -l $var ]
then
    echo ' '
else
    echo ' '
fi

```