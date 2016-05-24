### A formal system

Formal Systems are fairly common in computer programming - most of the problems we deal with are formal systems in some way.  This assignment addresses a system and in an applied way to not only better understand strict rule systems, but how we can use them to our advantage to better understand the boundaries of that system.

### A Puzzle

The M, I, and U puzzle is taken from the book *[Gödel, Escher, Bach](http://www.amazon.com/G%C3%B6del-Escher-Bach-Eternal-Golden/dp/0465026567)*.  It states that given a starting string of `MI` can you apply the rules below in an order to manipulate the string to become `MU`?

### Normal Mode

Write a program that attempts (in logic of your own design) to solve the `MU` puzzle. It can be any combination of hard coded rules, to randomness, a learning algorithm, or a brute for tree structure.


### Rules

Rule 1:  If you possess a string whose last letter is `I`, you can add on a `U` at the end.

Example:

```
Given:  MI
Output: MIU
```
Rule 2: If you have `Mx` then you can add `Mxx` to your string.

Example:

```
Given: MIU
Output: MIUIU

Given: MUM
Output: MUMUM
```

Rule 3: If `III` is present in your string, you can optionally convert it to `U`.  You may NOT convert a `U` to `III`.

Example:

```
Given: UMIIIMU
Output: UMUMU

Given: MIIII
Output: MIU (or MUI)
```

Rule 4: If `UU` occurs, you can drop it.

Example:

```
Given: UUU
Output: U

Given: MUUUIII
Output: MUIII
```

Extra Rule: Rules are one way - no inverse of any rule is allowed.

### Hard Mode

Implement an interpreter-like function that can take a string of instructions (rules) that will play through the "program" and output the state of the string at every instruction.  Yes, you are being asked to program your own finite state machine.

### Notes:

It is quite easy to find the solution to this program online... so PLEASE resist the temptation to find it. The reward is in the journey, not the treasure.
