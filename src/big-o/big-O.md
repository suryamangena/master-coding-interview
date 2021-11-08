## Big O
Big O talks about how long algorithm takes to run regardless of computer difference e.g. cpu 

## [Big O CheatSheet](./BigO-CheatSheet.pdf)

## [Big O Complexity Chart](./big-o.png)

## O(n) -> Linear Time -> No of elements increases No of Operations increases

## O(1) -> Constant Time 
Example 1:
```
function compressFirstBox(boxes){
    console.log(boxes[0]);
}
Here no of boxes given as input doesn't matter as it is only compressing first box
```
Example 2:
```
const boxes =[0,1,2,3,4,5];
function logFirstTwoBoxes(boxes){
    console.log(boxes[0]); // O(1)
    console.log(boxes[1]); //  O(1)
}
We don't care of O(1), O(2), O(3). we simply round this to O(1). O(1) is excellent as irrespective of input size elements time complexity is O(1)
```
Example 3: Calculate Big O for below problem,
```
function funChallenge(input) {
  let a = 10; // O(1)
  a = 50 + 3; // O(1)

  for (let i = 0; i < input.length; i++) { // O(n)
    anotherFunction(); // O(n)
    let stranger = true; //O(n)
    a++; //O(n)
  }
  return a; //O(1)
}

Big O Notation: O(3+4n)
```

Example 4: // What is the Big O of the below function? (Hint, you may want to go line by line)
```
function anotherFunChallenge(input) {
  let a = 5; // O(1)
  let b = 10; // O(1)
  let c = 50; // O(1)
  for (let i = 0; i < input; i++) { // O(n)
    let x = i + 1; // O(n)
    let y = i + 2; // O(n)
    let z = i + 3; // O(n)

  }
  for (let j = 0; j < input; j++) { // O(n)
    let p = j * 2; // O(n)
    let q = j * 2; // O(n)
  }
  let whoAmI = "I don't know"; O(1)
}

Big O Notation : O(4+7n)
In real time we won't add up like this instead of we simply mention as O(n) based on below rules
```

## [Big O Rule Book](./big-o-rules.png)
We can simplify the Big O by following the rules
## Big O Rule 1
1) Always consider the worst case 
```
//#1 -- For loop in Javascript.
const nemo = ['nemo','surya','sss','rrr'];
in other input nemo is last element of array, then Big O is O(n), if it is first element then O(1), in this case we always need to consider the worst case.

function findNemo1(array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i] === 'nemo') {
      console.log('Found NEMO!');
      break;
    }
  }
}

findNemo1(nemo);
```

## Big O Rule 2 -> Drop constants 
```
function printFirstItemThenFirstHalfThenSayHi100Times(items) {
    console.log(items[0]); // O(1)

    var middleIndex = Math.floor(items.length / 2); // O(1)
    var index = 0; //O(1)

    while (index < middleIndex) { //O(n/2)
        console.log(items[index]); //O(n/2)
        index++; //O(n/2)
    }

    for (var i = 0; i < 100; i++) { //O(100)
        console.log('hi');
    }
}

Big O: O(1+n/2+100)
As per drop constants rule, it becomes O(n).
```

## Big O Rule 3 -> Different terms for inputs
```
function compressBoxesTwice(boxes, boxes2){
  boxes.forEach(function(boxes){
    console.log(boxes);
  });


  boxes2.forEach(function(boxes){
    console.log(boxes);
  });
}

Big O Notation: O(a+b)
```

## 






