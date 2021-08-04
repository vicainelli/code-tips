# Javascript


## Conditionals

### Object Literals istead If-Else and Switch

Bad 👎 

```js
function getTranslation(rhyme) {
  if (rhyme.toLowerCase() === "apples and pears") {
    return "Stairs";
  } else if (rhyme.toLowerCase() === "hampstead heath") {
    return "Teeth";
  } else if (rhyme.toLowerCase() === "loaf of bread") {
    return "Head";
  } else if (rhyme.toLowerCase() === "pork pies") {
    return "Lies";
  } else if (rhyme.toLowerCase() === "whistle and flute") {
    return "Suit";
  }

  return "Rhyme not found";
}
```

Good 👍
```js
function getTranslationMap(rhyme) {
  const rhymes = {
    "apples and pears": "Stairs",
    "hampstead heath": "Teeth",
    "loaf of bread": "Head",
    "pork pies": "Lies",
    "whistle and flute": "Suit",
  };
  
  return rhymes[rhyme.toLowerCase()] ?? "Rhyme not found";
```

## Shorthands

### Declaring variables

```js
//Long version  
let a;   
let b = 1; 

//Shorthand  
let a, b = 1;
```

### Assigning values to multiple variables

```js
//Long version  
x = 1;   
y = 2;   
z = 3; 

//Shorthand  
let [x, y, z] = [1, 2, 3];
```




### Assigning default value

```js
let finalName;   
let name = getName();   
if(name !== null && name !== undefined && name !== '') {  
    finalName = name;   
} else {  
    finalName = 'Rahul'  
}

// Shorthand  
let finalName = getName() || 'Rahul';
```

### The ternary operator

```js
//Long version  
let points = 70;   
let result;   
if(marks >= 50){  
    result = 'Pass';   
}else{  
    result = 'Fail';   
}

//Shorthand  
let points = 70;   
let result = marks >= 50 ? 'Pass' : 'Fail';
```

### Template Literals

```js
// Long version  
console.log('Hello ' + name +', it is ' + day); 

//Shorthand  
console.log(`Hello ${name}, it is ${day}`);
```

### Swap two variables

```js
let x = 1, y = 2;   
//Long version  
const temp = x;   
x = y;   
y = temp; 

//Shorthand  
[x, y] = [y, x];
```

### AND(&&) Short circuit evaluation

```js
// Long version  
if (isLoggedin) {   
    redirectToHomepage();   
}

//Shorthand  
isLoggedin && redirectToHomepage();
```

### Arrow function

```js
//Long version  
function add(a, b) {  
    return a + b;   
}

// Shorthand  
const add = (a, b) => a + b;
```


### Multi-line string

```js
// Long version  
console.log('A blog is a discussion or informational website published\n' + 'on the World Wide Web consisting of discrete, often informal diary-style text entries. Posts are typically\n' + 'displayed in reverse chronological order, so that the most recent post\n' + 'appears first, at the top of the web page. Until 2009,\n' + 'blogs were usually the work of a single' ); 

//Shorthand  
console.log(`A blog is a discussion or informational website published on the World Wide Web consisting of discrete, often informal diary-style text entries . Posts are typically displayed in reverse chronological order, so that the most recent post appears first, at the top of the web page. Until 2009, blogs were usually the work of a single`);
```

### Multiple condition checking

```js
//Long version  
if (value === 1 || value === 'one' || value === 2 || value === 'two') {  
    //Execute code  
}

//Shorthand 1  
if ([1, 'one', 2, 'two'].indexOf(value) >= 0) {  
    //Execute code  
}  
//Shorthand 2  
if ([1, 'one', 2, 'two'].includes(value)) {  
    //Execute code  
}
```

### String into a number

```js
// Long version  
let total = parseInt('45');   
let average = parseFloat('421.6'); 

//Shorthand  
let total = +'45';   
let average = +'421.6';
```

### Object property Assignment

```js
let firstname = 'Emma';   
let lastname = 'Turner';   
//Long version  
let obj = {firstname: firstname, lastname: lastname}; 

//shorthand  
let obj = {firstname, lastname};
```

### Find max and min numbe rin array

```js
// Shorthand  
const arr = [2, 8, 15, 4];   
Math.max(...arr); // 15  
Math.min(...arr); // 2
```

### Exponent Power

```js
//Long version  
const power = Math.pow(4, 3); // 64

//Shorthand  
const power = 4**3; // 64
```

### Doouble NOT bitwise operator


```js
//Long version  
const floor = Math.floor(4.8); // 4

//Shorthand  
const floor = ~~4.8; // 4
```

### Repeat a string multiple time

```js
//Long version  
let str = '';   
for(let i = 0; i < 5; i ++) {  
    str += 'Hello ';   
}  
console.log(str); // Hello Hello Hello Hello Hello 

//Shorthand  
'Hello '.repeat(5);
```

### For loop

```js
let arr = [1, 2, 3, 4];   
//Long version  
for (let i = 0; 1 < arr.length; i++) {  
    console.log(arr[i]);   
}  
//Shorthand  
//for of loop  
for (const val of arr) {  
    console.log(val);   
}  
//for in loop  
for (const index in arr) {  
    console.log(arr[index]);  
}
```

### Deep clong of multi-level object

```js
let obj = {x: 20, y: {z: 30}}; 

//long version  
const makeDeepClone = (obj) => {  
    let newObject = {};   
    Object.keys(obj).map(key => {  
        if(typeof obj[key] === 'object'){  
            newObject[key] = make DeepClone(obj[key]);   
        } else {  
            newObject[key] = obj[key];   
        }  
    });   
    return neObject;   
}  
const cloneObj = makeDeepClone(obj); 

//Shorthand  
const cloneObj = JSON.parse(JSON.stringify(obj));
```

### Get character from string

```js
let str = 'heelloworld';   
//Long version  
str.charAt(1); // e

//Shorthand  
str[1]; // e
```

### Merging arrays

```js
let arr1 = [2, 3];   
//Long version  
let arr2 = arr1.concat([4, 5]);   
// [2, 3, 4, 5]

// Shorthand  
let arr2 = [...arr1, 4, 5];   
// [2, 3, 4, 5]
```
