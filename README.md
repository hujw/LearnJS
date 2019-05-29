# LearnJS
## var and let
Refer to [Use let with for Loops in JavaScript](https://wesbos.com/for-of-es6/)

* Use var
```
for(var i = 0; i < 10; i++) {
  console.log(i);
  setTimeout(function() {
    console.log('The number is ' + i);
  },1000);
}

C:\Program Files\nodejs\node.exe test.js 
0
1
2
3
4
5
6
7
8
9
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
The number is 10
```
The reason is console.log(i) will run immediately and reference whatever i is. However, after one second, this entire loop has already gone through every iteration that it needs to and the variable i here is being overwritten every single time.

* Use let
```
for(let i = 0; i < 10; i++) {
  console.log(i);
  setTimeout(function() {
    console.log('The number is ' + i);
  },1000);
}

C:\Program Files\nodejs\node.exe test.js 
0
1
2
3
4
5
6
7
8
9
The number is 0
The number is 1
The number is 2
The number is 3
The number is 4
The number is 5
The number is 6
The number is 7
The number is 8
The number is 9
```
