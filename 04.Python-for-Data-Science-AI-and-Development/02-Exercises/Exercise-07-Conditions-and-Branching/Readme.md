<center>
    <img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/Logos/organization_logo/organization_logo.png" width="300" alt="cognitiveclass.ai logo"  />
</center>

# Conditions in Python

Estimated time needed: **20** minutes

## Objectives

After completing this lab you will be able to:

-   work with condition statements in Python, including operators, and branching.


<h2>Table of Contents</h2>
<div class="alert alert-block alert-info" style="margin-top: 20px">
    <ul>
        <li>
            <a href="#cond">Condition Statements</a>
            <ul>
                <li><a href="comp">Comparison Operators</a></li>
                <li><a href="branch">Branching</a></li>
                <li><a href="logic">Logical operators</a></li>
            </ul>
        </li>
        <li>
            <a href="#quiz">Quiz on Condition Statement</a>
        </li>
    </ul>

</div>

<hr>


<h2 id="cond">Condition Statements</h2>


<h3 id="comp">Comparison Operators</h3>


Comparison operations compare some value or operand and, based on a condition, they produce a Boolean. When comparing two values you can use these operators:

<ul>
    <li>equal: <b>==</b></li>
    <li>not equal: <b>!=</b></li>
    <li>greater than: <b>></b></li>
    <li>less than: <b>&lt;</b></li>
    <li>greater than or equal to: <b>>=</b></li>
    <li>less than or equal to: <b>&lt;=</b></li>
</ul>


Let's assign <code>a</code> a value of 5. Use the equality operator denoted with two equal <b>==</b> signs to determine if two values are equal. The case below compares the variable <code>a</code> with 6.



```python
# Condition Equal

a = 5
a == 6
```




    False



The result is <b>False</b>, as 5 does not equal to 6.


Consider the following equality comparison operator <code>i > 5</code>. If the value of the left operand, in this case the variable <b>i</b>, is greater than the value of the right operand, in this case 5, then the statement is <b>True</b>. Otherwise, the statement is <b>False</b>.  If <b>i</b> is equal to 6, because 6 is larger than 5, the output is <b>True</b>.



```python
# Greater than Sign

i = 6
i > 5
```




    True



Set <code>i = 2</code>. The statement is false as 2 is not greater than 5:



```python
# Greater than Sign

i = 2
i > 5
```




    False



 Let's display some values for <code>i</code> in the figure. Set the values greater than 5 in green and the rest in red. The green region represents where the condition is **True**, the red where the statement is **False**. If the value of <code>i</code> is 2, we get **False** as the 2 falls in the red region. Similarly, if the value for <code>i</code> is 6 we get a **True** as the condition falls in the green region. 


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsGreater.gif" width="650" />


The inequality test uses an exclamation mark preceding the equal sign, if two operands are not equal then the condition becomes **True**.  For example, the following condition will produce **True** as long as the value of <code>i</code> is not equal to 6:



```python
# Inequality Sign

i = 2
i != 6
```




    True



When <code>i</code> equals 6 the inequality expression produces <b>False</b>. 



```python
# Inequality Sign

i = 6
i != 6
```




    False



See the number line below. when the condition is **True** the corresponding numbers are marked in green and for where the condition is **False** the corresponding number is marked in red.  If we set <code>i</code> equal to 2 the operator is true as 2 is in the green region. If we set <code>i</code> equal to 6, we get a **False** as the condition falls in the red region.


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsIneq.gif" width="650" />


 We can apply the same methods on strings. For example, use an equality operator on two different strings. As the strings are not equal, we get a **False**.



```python
# Use Equality sign to compare the strings

"ACDC" == "Michael Jackson"
```




    False



 If we use the inequality operator, the output is going to be **True** as the strings are not equal.



```python
# Use Inequality sign to compare the strings

"ACDC" != "Michael Jackson"
```




    True



Inequality operation is also used to compare the letters/words/symbols according to the ASCII value of letters. The decimal value shown in the following table represents the order of the character:


For example, the ASCII code for <b>!</b> is 33, while the ASCII code for <b>+</b> is 43. Therefore <b>+</b> is larger than <b>!</b> as 43 is greater than 33.


Similarly, the value for <b>A</b> is 65, and the value for <b>B</b> is 66 therefore:



```python
# Compare characters

'B' > 'A'
```




    True



 When there are multiple letters, the first letter takes precedence in ordering:



```python
# Compare characters

'BA' > 'AB'
```




    True



<b>Note</b>: Upper Case Letters have different ASCII code than Lower Case Letters, which means the comparison between the letters in python is case-sensitive.


<h3 id="branch">Branching</h3>


 Branching allows us to run different statements for different inputs. It is helpful to think of an **if statement** as a locked room, if the statement is **True** we can enter the room and your program will run some predefined tasks, but if the statement is **False** the program will ignore the task.


For example, consider the blue rectangle representing an ACDC concert. If the individual is older than 18, they can enter the ACDC concert. If they are 18 or younger than 18 they cannot enter the concert.

Use the condition statements learned before as the conditions need to be checked in the **if statement**. The syntax is as simple as <code> if <i>condition statement</i> :</code>, which contains a word <code>if</code>, any condition statement, and a colon at the end. Start your tasks which need to be executed under this condition in a new line with an indent. The lines of code after the colon and with an indent will only be executed when the **if statement** is **True**. The tasks will end when the line of code does not contain the indent.

In the case below, the tasks executed <code>print(“you can enter”)</code> only occurs if the variable <code>age</code> is greater than 18 is a True case because this line of code has the indent. However, the execution of <code>print(“move on”)</code> will not be influenced by the if statement.



```python
# If statement example

age = 19
#age = 18

#expression that can be true or false
if age > 18:
    
    #within an indent, we have the expression that is run if the condition is true
    print("you can enter" )

#The statements after the if statement will run regardless if the condition is true or false 
print("move on")
```

    you can enter
    move on


<i>Try uncommenting the age variable</i>


It is helpful to use the following diagram to illustrate the process. On the left side, we see what happens when the condition is <b>True</b>.  The person enters the ACDC concert representing the code in the indent being executed; they then move on. On the right side, we see what happens when the condition is <b>False</b>; the person is not granted access, and the person moves on. In this case, the segment of code in the indent does not run, but the rest of the statements are run. 


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsIf.gif" width="650" />


The <code>else</code> statement runs a block of code if none of the conditions are **True** before this <code>else</code> statement. Let's use the ACDC concert analogy again. If the user is 17 they cannot go to the ACDC concert,  but they can go to the Meatloaf concert.
The syntax of the <code>else</code> statement is similar as the syntax of the <code>if</code> statement, as <code>else :</code>. Notice that, there is no condition statement for <code>else</code>.
Try changing the values of <code>age</code> to see what happens:  



```python
# Else statement example

age = 18
# age = 19

if age > 18:
    print("you can enter" )
else:
    print("go see Meat Loaf" )
    
print("move on")
```

    go see Meat Loaf
    move on


The process is demonstrated below, where each of the possibilities is illustrated on each side of the image. On the left is the case where the age is 17, we set the variable age to 17, and this corresponds to the individual attending the Meatloaf concert. The right portion shows what happens when the individual is over 18, in this case 19, and the individual is granted access to the concert.


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsElse.gif" width="650" />


The <code>elif</code> statement, short for else if, allows us to check additional conditions if the condition statements before it are <b>False</b>. If the condition for the <code>elif</code> statement is <b>True</b>, the alternate expressions will be run. Consider the concert example, where if the individual is 18 they will go to the Pink Floyd concert instead of attending the ACDC or Meat-loaf concert. The person of 18 years of age enters the area, and as they are not older than 18 they can not see ACDC, but as they are 18 years of age, they attend  Pink Floyd. After seeing Pink Floyd, they move on. The syntax of the <code>elif</code> statement is similar in that we merely change the <code>if</code> in <code>if</code> statement to <code>elif</code>.



```python
# Elif statment example

age = 18

if age > 18:
    print("you can enter" )
elif age == 18:
    print("go see Pink Floyd")
else:
    print("go see Meat Loaf" )
    
print("move on")
```

    go see Pink Floyd
    move on


The three combinations are shown in the figure below.  The left-most region shows what happens when the individual is less than 18 years of age. The central component shows when the individual is exactly 18. The rightmost shows when the individual is over 18.


<img src ="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsElif.gif" width="650" />


 Look at the following code:



```python
# Condition statement example

album_year = 1983
album_year = 1970

if album_year > 1980:
    print("Album year is greater than 1980")
    
print('do something..')
```

    do something..


Feel free to change <code>album_year</code> value to other values -- you'll see that the result changes!


Notice that the code in the above <b>indented</b> block will only be executed if the results are <b>True</b>. 


As before, we can add an <code>else</code> block to the <code>if</code> block. The code in the <code>else</code> block will only be executed if the result is <b>False</b>.

<b>Syntax:</b> 

if (condition):

```
# do something
```

else:

```
# do something else
```


If the condition in the <code>if</code> statement is <b>False</b>, the statement after the <code>else</code> block will execute. This is demonstrated in the figure: 


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsLogicMap.png" width="650" />



```python
# Condition statement example

album_year = 1983
#album_year = 1970

if album_year > 1980:
    print("Album year is greater than 1980")
else:
    print("less than 1980")

print('do something..')
```

    Album year is greater than 1980
    do something..


Feel free to change the <code>album_year</code> value to other values -- you'll see that the result changes based on it!


<h3 id="logic">Logical operators</h3>


Sometimes you want to check more than one condition at once. For example, you might want to check if one condition and another condition is **True**. Logical operators allow you to combine or modify conditions.

<ul>
    <li><code>and</code></li>
    <li><code>or</code></li>
    <li><code>not</code></li>
</ul>

These operators are summarized for two variables using the following truth tables:  


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsTable.png" width="650" />


The <code>and</code> statement is only **True** when both conditions are true. The <code>or</code> statement is true if one condition is **True**. The <code>not</code> statement outputs the opposite truth value.


Let's see how to determine if an album was released after 1979 (1979 is not included) and before 1990 (1990 is not included). The time periods between 1980 and 1989 satisfy this condition. This is demonstrated in the figure below. The green on lines <strong>a</strong> and <strong>b</strong> represents periods where the statement is **True**. The green on line <strong>c</strong> represents where both conditions are **True**, this corresponds to where the green regions overlap. 


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsEgOne.png" width="650" />


 The block of code to perform this check is given by:



```python
# Condition statement example

album_year = 1980

if(album_year > 1979) and (album_year < 1990):
    print ("Album year was in between 1980 and 1989")
    
print("")
print("Do Stuff..")
```

    Album year was in between 1980 and 1989
    
    Do Stuff..


To determine if an album was released before 1980 (~ - 1979) or after 1989 (1990 - ~), an **or** statement can be used. Periods before 1980 (~ - 1979) or after 1989 (1990 - ~) satisfy this condition. This is demonstrated in the following figure, the color green in <strong>a</strong> and <strong>b</strong> represents periods where the statement is true. The color green in **c** represents where at least one of the conditions 
are true.  


<img src="https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%203/Images/CondsEgTwo.png" width="650" />


The block of code to perform this check is given by:



```python
# Condition statement example

album_year = 1990

if(album_year < 1980) or (album_year > 1989):
    print ("Album was not made in the 1980's")
else:
    print("The Album was made in the 1980's ")
```

    Album was not made in the 1980's


The <code>not</code> statement checks if the statement is false:



```python
# Condition statement example

album_year = 1983

if not (album_year == '1984'):
    print ("Album year is not 1984")
```

    Album year is not 1984


<hr>


<h2 id="quiz">Quiz on Conditions</h2>


Write an if statement to determine if an album had a rating greater than 8. Test it using the rating for the album <b>“Back in Black”</b> that had a rating of 8.5. If the statement is true print "This album is Amazing!"



```python
# Write your code below and press Shift+Enter to execute
rating=8.5
if rating>8:
    print("This Albumn is Great")
```

    This Albumn is Great


<details><summary>Click here for the solution</summary>

```python
rating = 8.5
if rating > 8:
    print ("This album is Amazing!")
```

</details>


<hr>


Write an if-else statement that performs the following. If the rating is larger then eight print “this album is amazing”. If the rating is less than or equal to 8 print “this album is ok”.



```python
# Write your code below and press Shift+Enter to execute
rating=8.5
if rating>8:
    print("This albumn is great")
else:
    Print("this albumn is ok")
```

    This albumn is great


<details><summary>Click here for the solution</summary>

```python
rating = 8.5
if rating > 8:
    print ("this album is amazing")
else:
    print ("this album is ok")
    
```

</details>


<hr>


Write an if statement to determine if an album came out before 1980 or in the years: 1991 or 1993. If the condition is true print out the year the album came out.



```python
# Write your code below and press Shift+Enter to execute
date=1979
if date<1980 or date==1991 or date== 1993:
    print("This albumn came out in the year %d"%date)
```

    This albumn came out in the year 1979


<details><summary>Click here for the solution</summary>

```python
album_year = 1979

if album_year < 1980 or album_year == 1991 or album_year == 1993:
    print ("This album came out in year %d" %album_year)
    
```

</details>


<hr>
<h2>The last exercise!</h2>
<p>Congratulations, you have completed your first lesson and hands-on lab in Python. However, there is one more thing you need to do. The Data Science community encourages sharing work. The best way to share and showcase your work is to share it on GitHub. By sharing your notebook on GitHub you are not only building your reputation with fellow data scientists, but you can also show it off when applying for a job. Even though this was your first piece of work, it is never too early to start building good habits. So, please read and follow <a href="https://cognitiveclass.ai/blog/data-scientists-stand-out-by-sharing-your-notebooks/" target="_blank">this article</a> to learn how to share your work.
<hr>


## Author

<a href="https://www.linkedin.com/in/joseph-s-50398b136/" target="_blank">Joseph Santarcangelo</a>

## Other contributors

<a href="www.linkedin.com/in/jiahui-mavis-zhou-a4537814a">Mavis Zhou</a>

## Change Log

| Date (YYYY-MM-DD) | Version | Changed By | Change Description                 |
| ----------------- | ------- | ---------- | ---------------------------------- |
| 2020-08-26        | 2.0     | Lavanya    | Moved lab to course repo in GitLab |
|                   |         |            |                                    |
|                   |         |            |                                    |

<hr/>

## <h3 align="center"> © IBM Corporation 2020. All rights reserved. <h3/>

