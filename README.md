# perceptron-bipolar-and
A basic implementation of logical 'and' in a Perceptron

## Setup
```
$ python3 -m venv venv
$ source ./venv/bin/activate
$ pip install -r requirements.txt
```

## Test
```
$ python3 Perceptron_Test.py
```

## Static Analysis
```
$ pycodestyle *.py
```

Loosely based on "Artificial Neural Networks | Implementation of AND function Using PERCEPTRON Model" by Dr. Krishan Kumar, https://www.youtube.com/watch?v=Pzwh0uofKJw&t=1158s


## Sample Output
```
(venv) (base) shirish@***************:workarea/perceptron-logical-and ‹master›$ python3 Perceptron_Test.py
------------------------------------------------------------------------
             Input   Tar NetIP CalOP         WtChanges           Weights
    x1    x2    LR     t  y_in     y   dw1   dw2    db    w1    w2     b
------------------------------------------------------------------------
Epoch-1
     1     1     1     1     0     0     1     1     1    a 1     1     1
     1    -1     1    -1     1     1    -1     1    -1     0     2     0
    -1     1     1    -1     2     1     1    -1    -1     1     1    -1
    -1    -1     1    -1    -3    -1   ---   ---   ---     1     1    -1
   (Y)     ^
         5 |
4.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
3.66666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
         3 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
2.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
1.66666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
         1 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
0.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-0.3333333 | ⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⡗⠒⠒⠲⡒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒
        -1 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠈⠢⡀⠀⠀⠀⠀⠀⠀⠀⠀
-1.6666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠈⠢⡀⠀⠀⠀⠀⠀⠀
-2.3333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠈⠂⠀⠀⠀⠀⠀
        -3 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-3.6666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-4.3333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
        -5 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-----------|-|---------|---------|---------|-> (X)
           | -5        -1.666667 1.6666667 5



------------------------------------------------------------------------
             Input   Tar NetIP CalOP         WtChanges           Weights
    x1    x2    LR     t  y_in     y   dw1   dw2    db    w1    w2     b
------------------------------------------------------------------------
Epoch-2
     1     1     1     1     1     1   ---   ---   ---     1     1    -1
     1    -1     1    -1    -1    -1   ---   ---   ---     1     1    -1
    -1     1     1    -1    -1    -1   ---   ---   ---     1     1    -1
    -1    -1     1    -1    -3    -1   ---   ---   ---     1     1    -1
   (Y)     ^
         5 |
4.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
3.66666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
         3 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
2.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
1.66666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
         1 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
0.33333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-0.3333333 | ⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒⡗⠒⠒⠲⡒⠒⠒⠒⠒⠒⠒⠒⠒⠒⠒
        -1 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠈⠢⡀⠀⠀⠀⠀⠀⠀⠀⠀
-1.6666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠈⠢⡀⠀⠀⠀⠀⠀⠀
-2.3333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠈⠂⠀⠀⠀⠀⠀
        -3 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-3.6666667 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-4.3333333 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
        -5 | ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
-----------|-|---------|---------|---------|-> (X)
           | -5        -1.666667 1.6666667 5



evaluate    1   1 , result:  (1, 1)
evaluate   -1   1 , result:  (-1, -1)
evaluate    1  -1 , result:  (-1, -1)
evaluate   -1  -1 , result:  (-1, -3)
.
----------------------------------------------------------------------
Ran 1 test in 0.009s

OK
```
