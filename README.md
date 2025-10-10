<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name: KAVIPRIYA S.P            </h3>
<h3>Register Number: 2305002011         </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


<h2>Algorithm:</h2>
<p>
<ol>
 <li> Generate a random initial solution of the same length as the target.</li> 
<li>Calculate the score as the ASCII difference between solution and target.</li>
 <li>If the score is zero, stop (solution found).</li>
 <li>Mutate the solution by changing one random character.</li>
 <li>Accept the new solution if its score is better, otherwise repeat.</li>
</ol>
</p>
<hr>
<h3> Steps Applied:</h3>
<h3>Step-1</h3>
<p> Generate Random String of the length equal to the given String</p>
<h3>Step-2</h3>
<p>Mutate the randomized string each character at a time</p>
<h3>Step-3</h3>
<p> Evaluate the fitness function or Heuristic Function</p>
<h3>Step-4:</h3>
<p> Lopp Step -2 and Step-3  until we achieve the score to be Zero to achieve Global Minima.</p>

## PROGRAM
```python
import random, string

answer = "Artificial Intelligence"
gen = lambda: [random.choice(string.printable) for _ in range(len(answer))]
score = lambda s: sum(abs(ord(a)-ord(b)) for a,b in zip(s,answer))

best = gen()
while True:
    print("Score:", score(best), "Solution:", "".join(best))
    if score(best) == 0: break
    new = best[:]; new[random.randrange(len(answer))] = random.choice(string.printable)
    if score(new) < score(best): best = new
```

<hr>
<h2>Output:</h2>
<img width="611" height="728" alt="image" src="https://github.com/user-attachments/assets/5a7861ef-99cb-450f-a86a-1ba78b834dcc" />
<img width="408" height="693" alt="image" src="https://github.com/user-attachments/assets/5570dedb-e40d-4296-bd4a-f91dec0ada76" />


<h3>RESULT:</h3>
<p>Thus the program to Implement Simple Hill Climbing Algorithm has been executed successfully. </p>
