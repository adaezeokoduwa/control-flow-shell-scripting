# control-flow-shell-scripting

# Control Flow in Shell Scripting - Practice Summary

## What is Control Flow in Shell Scripting?

Control flow in shell scripting refers to the ability to control the execution path of commands based on conditions or loops. It helps scripts make decisions (`if`, `elif`, `else`), perform repetitive actions (`while`, `for` loops), and react based on user input or logic.

Control flow is essential for making shell scripts more dynamic and intelligent â€” instead of just running commands in order, the script can "think" and “decide” what to do next.what to do next.

---

## Tasks Practiced Step-by-Step Explanation

### Task 1: Echo and Input Handling

**Objective:** Write a script that accepts a number as input and displays a message.

**What I did:**

- I created a shell script using `nano`:
  ```
  nano control_flow.sh
  ```

- Inside the file, I added:
  ```
  #!/bin/bash
  read -p "Enter a number: " num
  echo "You have entered the number $num"
  ```

- This used `read` to take input from the user, and `echo` to display the entered number.

- I made it executable:
  ```
  chmod +x control_flow.sh
  ```

- Then ran it:
  ```
  ./control_flow.sh
  ```
![](https://github.com/adaezeokoduwa/control-flow-shell-scripting/blob/main/imgs/flow11.jpg?raw=true)
![](https://github.com/adaezeokoduwa/control-flow-shell-scripting/blob/main/imgs/flow11.jpg?raw=true)

### Task 2: Using `if` Statement

**Objective:** Check if a number is positive.

**What I did:**

- I added an `if` statement:
  ```
  if [ "$num" -gt 0 ]; then
      echo "The number is positive."
  fi
  ```

- This checks if the entered number is greater than zero, using the `-gt` (greater than) comparison.

- The full script now looks like:
  ```bash
  #!/bin/bash
  read -p "Enter a number: " num
  echo "You have entered the number $num"

  if [ "$num" -gt 0 ]; then
      echo "The number is positive."
  fi
  ```

### Task 3: Using `elif` and `else` Statements

**Objective:** Check if a number is negative or zero.

**What I did:**

- I extended the script using `elif` and `else`:
  ```
  if [ "$num" -gt 0 ]; then
      echo "The number is positive."
  elif [ "$num" -lt 0 ]; then
      echo "The number is negative."
  else
      echo "The number is zero."
  fi
  ```

- Now, the script makes a full decision:
  - If number > 0 - positive
  - If number < 0 - negative
  - If number = 0 - zero

### Task 4: Testing and Debugging

**What I practiced:**

- I tested the script with:
  - A **positive number** (e.g. 5) - Got "The number is positive"
  - A **negative number** (e.g. -3) - Got "The number is negative"
  - The number **0** - Got "The number is zero"

- I learned to quote variables like `"$num"` to prevent errors when no input is entered.

- I fixed syntax errors like:
  - Missing spaces in `[ "$num" -gt 0 ]`
  - Missing `then` keyword

---



##   What I Learned

- How to create and execute shell scripts
- How to accept and process user input
- How to use conditionals to control program flow
- How to debug basic shell script errors
- The importance of correct syntax and quoting variables

---
![](https://github.com/adaezeokoduwa/control-flow-shell-scripting/blob/main/imgs/flow3.jpg?raw=true)
## Sample Final Script

```
#!/bin/bash

read -p "Enter a number: " num
echo "You have entered the number $num"

if [ "$num" -gt 0 ]; then
    echo "The number is positive."
elif [ "$num" -lt 0 ]; then
    echo "The number is negative."
else
    echo "The number is zero."
fi
```

This script is a practical demonstration of **control flow** in bash using `if`, `elif`, and `else`.

---
### Task 2: Loop - Repeating Commands

**Objective:** Practice how to repeat a command multiple times using a loop in bash scripting.

---

##  What I Did:

I created a shell script to understand how a `while` loop works. A `while` loop is useful when you want to run a block of code **as long as a condition is true**.

---

### Step-by-Step Process:

1. I opened my terminal and created a new script file:
   ```
   nano loop.sh
   ```

2. Then I typed the following loop code:

  ```
   #!/bin/bash
   
   for i in 1 2 3 4 5
  do 
  echo "Hello, World! This is message $i"
  done
  ```

3. I saved and closed the editor:
   - Pressed `CTRL + O`, then `Enter` to save
   - Pressed `CTRL + X` to exit

4. I made the script executable:
   ````
   chmod +x loop.sh
   ````

5. I ran the script:
   ````
   ./loop.sh
   ````

---
### What Happened:

When I executed the script, the terminal printed:

```
Hello, World! This is message 1
Hello, World! This is messager 2
Hello, World! This is message 3
Hello, World! This is messager 4
Hello, World! This is message 5
```
---

##  What I Learned:

- How to use the `while` loop in bash scripting.
- How to initialize a variable (`count=1`).
- How to check conditions with `[ $count -le 5 ]`.
- How to increment a variable using `((count++))`.

![](https://github.com/adaezeokoduwa/control-flow-shell-scripting/blob/main/imgs/loop11.jpg?raw=true)

![](https://github.com/adaezeokoduwa/control-flow-shell-scripting/blob/main/imgs/loop22.jpg?raw=true)
## Conclusion

This exercise helped me understand how bash scripts make decisions and respond to different inputs. Practicing control flow makes me more confident in writing scripts that are interactive and useful in real-world automation.



