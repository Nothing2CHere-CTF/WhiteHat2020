# WhiteHat Grand Prix 06 (2020)
WhiteHat Grand Prix - 06 - 2020

## Overview

**URL:** https://grandprix.whitehatvn.com/  
**Organisors:** Vietnam Today
**Duration:** 24 hours  
**Team mates:** Team Competition  

```
Title                         Category        Points  Flag
----------------------------- --------------- ------- ------------------------------------------
Programming 01                  Prog            100    WhiteHat{BO0l3_1s_s1MpL3_f0R_Pr0gR4mM3R}
```
## Prog3

* **Category:** Prog
* **Points:** 100

### Challenge

```
Very well, can you figure it out?
A * A = A
A + A = A

(A * B) * C = A * (B * C)
(A + B) + C = A + (B + C)

A * B = B * A
A + B = B + A

A * (B + C) = A * B + A * C
A + (B * C) = (A + B) * (A + C)

A * 0 = 0; A * 1 = A
A + 1 = 1; A + 0 = A

A * ~A = 0
A + ~A = 1

~(~A) = A

~(A * B) = ~A + ~B
~(A + B) = ~A * ~B

Given two expressions, are they equal? Enter either [YES/NO]
```

> Boolean Algebra.
>
> nc 52.78.36.66 82



### Solution

[BExpred.jar](/WhiteHat2020/BExpred.jar)

Connecting to 52.78.36.66 on port 82, a series of 18 random pairs of boolean algrebraic equations is presented to which the answer YES is expected if the two equations are equivalent, or NO if they are not.

Initially, I simply tried simplifying the equations via https://www.dcode.fr/boolean-expressions-calculator, but for longer equations, an error was presented [dcode_boolean_calc.png](WhiteHat2020/dcode_boolean_calc.png)

Via https://stackoverflow.com/questions/14902141/any-good-boolean-expression-simplifiers-out-there/14903388, I came across https://sourceforge.net/projects/bexpred/, a java program which includes a tool called Expression Compare.  This tool allows for pasting equations into each field, and produces a True or False response.

Since the server didn't issue any timeouts, I was not forced to do any programming in this challenge, but simply copied the text of E1 and E2 from the netcat terminal and pasted them into the java tool.  For each True response, I typed YES into the terminal, and NO for False responses.

After 18 challenges, the following text was returned: 
Very well, you've done it the right way! Your flag is: WhiteHat{BO0l3_1s_s1MpL3_f0R_Pr0gR4mM3R}

I don't think I did, but then I didn't *have* to do it "the right way" :)


**Flag**
```
Plain Text: WhiteHat{BO0l3_1s_s1MpL3_f0R_Pr0gR4mM3R}
SHA1: WhiteHat{1b3e3988b57be0777621d6eda3db6c3b02a90de4}
```
---
