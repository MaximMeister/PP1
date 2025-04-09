# PP1

## Goal
All PPn practical exercises share a common purpose: to help you demonstrate—step by step—that you followed and understood the content presented in the weekly lectures. This ongoing feedback loop allows me, as your lecturer, to monitor your personal progress.

In this first exercise, your goal is to demonstrate an understanding of digital computation: specifically, how to map elements of an input set to an output set. We'll begin with simple mappings and gradually increase the difficulty.

**Important:** Start a stopwatch when you begin and work uninterruptedly for 90 minutes. Once time is up, stop immediately and document the point where you had to pause.

---

## Workflow
Each exercise will follow the same basic workflow:

1. **Fork** the repository
2. **Modify and Commit** your solution
3. **Submit your link for Review**

### Step 1: Fork the Repository
A fork is a personal copy of this repository under your own GitHub account. You can edit and manage it freely. Even if you make mistakes, you can always restart or revisit your progress.

To fork this repository:

1. Create a GitHub account (you may use your university email).
2. Open this project in your browser.
3. Click the `Fork` button in the top-right corner:

   ![Fork-Button](./assets/fork.png)

---

4. Scroll down in the dialog and click `Create fork`:

   ![Create fork-Button](./assets/create_fork.png)

---

### Step 2: Modify and Commit
A **commit** is a saved snapshot of your work.

1. Navigate to the `README.md` file.
2. Click the pencil icon to edit the file:

   ![Pencil-Button](./assets/pencil.png)

---

3. Use the built-in editor to make changes.
4. Click `Commit changes` when done:

   ![Commit-Button](./assets/commit_button.png)

---

Add a meaningful comment about what you did and how long it took.

### Step 3: Submit for Review
If you get stuck, visit the discussions forum:
[https://github.com/MaxClerkwell/PP1/discussions](https://github.com/MaxClerkwell/PP1/discussions)

When you have finished working, in Moodle, click "Add solution" and submit the link to your repository.

---

## Tasks

### Task 1: Mapping Symbols to Binary
Fill out the following table, mapping decimal numbers `0` through `15` to their binary representations:

| Decimal | Binary Representation |
|---------|------------------------|
| 0       | 0000                   |
| 1       | 0001                   |
| 2       | 0010                   | 
| 3       | 0011                   | 
| 4       | 0100                   | 
| 5       | 0101                   |     
| 6       | 0110                   |    
| 7       | 0111                   | 
| 8       | 1000                   | 
| 9       | 1001                   |     
| 10      | 1010                   |    
| 11      | 1011                   | 
| 12      | 1100                   | 
| 13      | 1101                   |     
| 14      | 1110                   |                 
| 15      | 1111                   |

**How many binary digits (bits) are needed?**
The numbers 0 to 15 (in decimal) can be represented with 4 bits.

Explain how to calculate the number of bits required:
<details>
<summary>Your Answer</summary>
There are only 2 possible states of a digit / bit: 0 or 1
Therefore the equation: 2<sup>n</sup> (n= amount of bits) shows the highest possible number in decimal.
    
To calculate the needed bits for any decimal number the following equation has to be used:

n=⌊log<sub>2</sub> (x)⌋+1

as example 53 (dec)

n=⌊log<sub>2</sub> (53)⌋+1=⌊5.73⌋+1=5+1 =6

Explanations
- ⌊...⌋ => means rounded down to the next whole number
- +1 => is needed for the maximum value in the range is included

</details>

---

### Task 2: Mapping Binary to Binary
Digital processors implement **logical functions** using **logic gates** like NAND, AND, OR, etc.
These functions map binary input sets (voltages) to binary outputs.

Refer to the truth table of a 1-bit full adder:

| C<sub>in</sub> | B | A | Sum (S) | C<sub>out</sub> |
|--------------|---|---|---------|-----------------|
| 0            | 0 | 0 | 0       | 0               |
| 0            | 0 | 1 | 1       | 0               |
| 0            | 1 | 0 | 1       | 0               |
| 0            | 1 | 1 | 0       | 1               |
| 1            | 0 | 0 | 1       | 0               |
| 1            | 0 | 1 | 0       | 1               |
| 1            | 1 | 0 | 0       | 1               |
| 1            | 1 | 1 | 1       | 1               |

> Simulate this adder using NAND gates:
[Full Adder NAND CircuitVerse Project](https://circuitverse.org/users/305021/projects/full-adder-nand-990621f6-993b-4676-a1b5-2a31aae451ce)

#### Your Task
Create a truth table for a **2-bit adder** without carry-in. What are the possible inputs and outputs?

| A1A0 | B1B0 | A (dec) | B (dec) | Sum (dec) | Sum (bin) |
|------|------|---------|---------|-----------|-----------|
|  00  |  00  |   0     |   0     |     0     | 000       |
|  00  |  01  |   0     |   1     |     1     | 001       |
|  00  |  10  |   0     |   2     |     2     | 010       |
|  00  |  11  |   0     |   3     |     3     | 011       |
|  01  |  00  |   1     |   0     |     1     | 001       |
|  01  |  01  |   1     |   1     |     2     | 010       |
|  01  |  10  |   1     |   2     |     3     | 011       |
|  01  |  11  |   1     |   3     |     4     | 100       |
|  10  |  00  |   2     |   0     |     2     | 010       |
|  10  |  01  |   2     |   1     |     3     | 011       |
|  10  |  10  |   2     |   2     |     4     | 100       |
|  10  |  11  |   2     |   3     |     5     | 101       |
|  11  |  00  |   3     |   0     |     3     | 011       |
|  11  |  01  |   3     |   1     |     4     | 100       |
|  11  |  10  |   3     |   2     |     5     | 101       |
|  11  |  11  |   3     |   3     |     6     | 110       |

Because I wasnt sure, after I read task 3 (there is mentioned the Output C<sub>out<sub>

| A1 | A0 | B1 | B0 | Cout | Sum1  | Sum0  |
|----|----|----|----|------|-------|-------|
|  0 |  0 |  0 |  0 |   0  |   0   |   0   |
|  0 |  0 |  0 |  1 |   0  |   0   |   1   |
|  0 |  0 |  1 |  0 |   0  |   1   |   0   |
|  0 |  0 |  1 |  1 |   0  |   1   |   1   |
|  0 |  1 |  0 |  0 |   0  |   0   |   1   |
|  0 |  1 |  0 |  1 |   0  |   1   |   0   |
|  0 |  1 |  1 |  0 |   0  |   1   |   1   |
|  0 |  1 |  1 |  1 |   1  |   0   |   0   |
|  1 |  0 |  0 |  0 |   0  |   1   |   0   |
|  1 |  0 |  0 |  1 |   0  |   1   |   1   |
|  1 |  0 |  1 |  0 |   1  |   0   |   0   |
|  1 |  0 |  1 |  1 |   1  |   0   |   1   |
|  1 |  1 |  0 |  0 |   0  |   1   |   1   |
|  1 |  1 |  0 |  1 |   1  |   0   |   0   |
|  1 |  1 |  1 |  0 |   1  |   0   |   1   |
|  1 |  1 |  1 |  1 |   1  |   1   |   0   |

---

### Task 3: Boolean Equations via Karnaugh Maps
Use the [K-Map method](https://github.com/STEMgraph/4b957490-badf-4264-b9f2-1b5aa370f36e) to derive Boolean equations for each output bit in your 2-bit adder.

1. Fill out Karnaugh Maps
2. Write down an equation for each cell marked `1`
3. 
4. Combine them using OR gates
5. Minimize the equations

Q<sub>0</sub> or Sum<sub>1<sub>
| A\B     | 00 | 01 | 11 | 10 |
|---------|----|----|----|----|
| 00      | 0  | 0  | 1  | 1  |
| 01      | 0  | 1  | 0  | 1  |
| 11      | 1  | 1  | 0  | 0  |
| 10      | 1  | 1  | 1  | 0  |

Q<sub>1</sub> or Sum<sub>0<sub>
| A\B     | 00 | 01 | 11 | 10 |
|---------|----|----|----|----|
| 00      | 0  | 1  | 1  | 0  |
| 01      | 1  | 0  | 0  | 1  |
| 11      | 1  | 0  | 0  | 1  |
| 10      | 0  | 1  | 1  | 0  |

C<sub>out</sub> 
| A\B     | 00 | 01 | 11 | 10 |
|---------|----|----|----|----|
| 00      | 0  | 0  | 0  | 0  |
| 01      | 0  | 0  | 1  | 0  |
| 11      | 0  | 1  | 1  | 1  |
| 10      | 0  | 0  | 1  | 1  |

<details>
<summary>The final functions</summary>

Q<sub>0</sub> = Q0 = A1' *A0' *B1 + A1'*A0*B1*B0' + A1'*A0*B1'*B0 + A1*A0'* B1' + A1*A0*B0 + A1*A0*B1*B0

Q<sub>1</sub> =  A0 + B0

C<sub>out</sub> = (A0 *B1* B0)+(A1* B1) + (A1* A0 * B0)


</details>

---

### Task 4: Circuit Implementation
Using your Boolean equations, build a logic network in [CircuitVerse](https://circuitverse.org) that implements at least one bit of the adder.

<details>
<summary>Your solution</summary>
A share link to your solution goes here: <a href="<iframe src="https://circuitverse.org/simulator/embed/maxim-meister-bit-adder-5c6f7a87-9e28-4437-8ed6-b5a910b12329?theme=&display_title=false&clock_time=true&fullscreen=true&zoom_in_out=true" style="border-width:; border-style: ; border-color:;" name="myiframe" id="projectPreview" scrolling="no" frameborder="1" marginheight="0px" marginwidth="0px" height="500" width="500" allowFullScreen></iframe>

or try this:

https://circuitverse.org/simulator/embed/maxim-meister-bit-adder-5c6f7a87-9e28-4437-8ed6-b5a910b12329
   
   ">Link!</a>
</details>

---

**Remember:** Stop working after 90 minutes and record where you stopped!

