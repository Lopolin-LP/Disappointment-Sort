# Disappointment Sort
A sorting algorithm I came up with. It's not good at being a sorting algorithm.

## Idea
Sort out all the things that aren't in order. Then, one by one, insert them back into their correct place.

## Practical application
Probably only in real life where computer sorting algorithms aren't easy to use.

## Example
Starting with
1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10
-|-|-|-|-|-|-|-|-|-
6 | 10 | 0 | 11 | 10 | 9 | 9 | 14 | 19 | 11

### Level 1A
...it becomes already sorted; we turn it into
1 | 2 | 3 | 4 | 5
-|-|-|-|-
6 | 10 | 11 | 14 | 19

and our unsorted stuff will be

1 | 2 | 3 | 4 | 5
-|-|-|-|-
0 | 10 | 9 | 9 | 11

Then we take the second one and go through it as well.

### Level 2A
This gets us

1 | 2 | 3
-|-|-
0 | 10 | 11

1 | 2
-|-
9 | 9

### Level 3
Now let's do the shorted bubble sort in history, and compare if the second number is bigger than the first. If so, return them reversed, otherwise keep as is.

We return as is.

### Level 2B
Now we insert the sorted queue back into our array. We can do this by going over each number and checking if the current number in queue is smaller than the one we're at. If so, we insert the number and check it again, but with the next in queue. If not, we go to the next number in the array.

1 | 2 | 3 | 4 | 5
-|-|-|-|-
0 | 9 | 9 | 10 | 11

### Level 1B
Now let's do that here too, remember, our current array is

1 | 2 | 3 | 4 | 5
-|-|-|-|-
6 | 10 | 11 | 14 | 19

and our queue is

1 | 2 | 3 | 4 | 5
-|-|-|-|-
0 | 9 | 9 | 10 | 11

so our output is

1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10
-|-|-|-|-|-|-|-|-|-
0 | 6 | 9 | 9 | 10 | 10 | 11 | 11 | 14 | 19

### End
And it's sorted! Now keep in mind that this is very inefficient for computers, so don't use it there!
