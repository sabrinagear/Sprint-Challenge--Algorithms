###Excercise I

a) O(n) - Tricky. Okay so would normally be O(n^3) but since since a=0 we add n^2 to a each time, making it more like a for loop.

b) If we break this down line by line:

| Line                           | Big O |
| ------------------------------ | ----- |
| for i in range(n):             | n     |
| i += 1                         | 1     |
| for j in range(i + 1, n):      | n     |
| k += 1                         | 1     |
| for l in range(k + 1, 10 + k): | n     |
| l += 1                         | 1     |
| sum += 1                       | 1     |

Multiply and reduce.

Answer: O(n^3)

c) Following the same logic as question a, this has a runtime of O(n)

###Excercise II

a) Define the problem

_f_ = floor at which an egg will break

For an _n_ story building, find _f_ as efficiently as possible.

b) Solve the problem

This would be best solved using a binary tree.

Start halfway up the building. Drop the egg. If it breaks, you can eliminate every floor above that floor, thus cutting the problem in half. Repeat this until you find your target.

The runtime complexity? log2(n)
