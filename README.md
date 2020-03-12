# Project Shift Coding Challenge

CHALLENGE #1
```
function cityStatus(){
  console.log('Durham is awesome!');
};

cityStatus();
```


CHALLENGE #2
```
const bands = ['Kiss', 'Aerosmith', 'ACDC', 'Led Zeppelin', 'Nickelback']

for (let i = 0; i < bands.length; i++ ){
  alert('I love ' + bands[i]+'!')
};
```


CHALLENGE #3
```
const bands = ['Kiss', 'Aerosmith', 'ACDC', 'Led Zeppelin', 'Nickelback']

if(bands.indexOf("Nickelback") !== -1){
  bands.pop("Nickelback"); //get outta here
for (let i = 0; i < bands.length; i++){ 
  alert('I love ' + bands[i]+'!');
  alert("I DON'T love Nickelback!")
};
```

CHALLENGE #4
```
const array = [34, 203, 16, 46, 34, 432, 342, 124, 33, 188, 12]

let average = array.reduce(function (sum, value) {
        return sum + value;
    }, 0) / array.length;

console.log(Math.floor(average));
```

CHALLENGE #5
```
const array = ['a', 'b', 'c', 'd', 'c', 'b', 'b', 'c', 'a', 'e', 'b', 'e'];

let findMost = function findMost(array){
    return array.sort((a,b) =>
          array.filter(v => v===a).length
        - array.filter(v => v===b).length
    ).pop();
    return;
};

let findLeast = function findLeast(array){
    return array.sort((a,b) =>
          array.filter(v => v===a).length
        - array.filter(v => v===b).length
    ).shift();
    return;
};

console.log(`most: ` + (findMost(array)));
console.log(`least: ` + (findLeast(array)));
```


CHALLENGE #6
```
const arr1 = ['a', 'b', 'c', 'a', 'a', 'b', 'd'];
const arr2 = ['a', 'b', 'b', 'a', 'e', 'c', 'c', 'g'];

const checkInArray = (arr,value) => {
    let count=0
    arr.forEach((el)=>{
        if(el == value)
            count++
    })
    return count;
}

/* 



Full disclosure: everything after this is with the help of a coder friend and his co-worker going way over my head with maps. I could not figure out how to replicate the result as it is listed and not in alphabetical order.



*/

const buildOverlap = (mapA,mapB) => {
  let count = 0;
  let c = '';
for (const valA in mapA) {
    if(mapB.hasOwnProperty(valA)){
      count = mapB[valA] > mapA[valA] ? mapA[valA] : mapB[valA]
          let i = 0;
            while(i < count){
                c = c.concat(valA)            
                i++;
            }
    }
  }
    return c.split('');
}

//Iknowsomeofthesewords.gif

const run = () => {
    let mapA = {};
    let mapB = {};
 
    a.forEach((el,idx) => {
      mapA[el] = checkInArray(a,el)
    })

    b.forEach((el,idx) => {
      mapB[el] = checkInArray(b,el)
    })

    return buildOverlap(mapA,mapB)
}

let a =['a', 'b', 'c', 'a', 'a', 'b', 'd'];
let b = ['a', 'b', 'b', 'a', 'e', 'c', 'c', 'g'];

let response = run(a,b);
console.log(response)
```


CHALLENGE #7
```
function theLoot(cost) {
  let change = [0, 0, 0]
  while (cost >= 100){
    cost -= 100
    change[0]++
  }
  while (cost >= 20){
    if (cost % 50 === 0){break}
    cost -= 20
    change[1]++
  }
  while (cost <= 19){
    if (cost <= 0){break}
    cost -= 1
    change[2]++
  }
  return change
};

console.log(theLoot(125));
```
