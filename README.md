# `What I Learned in Week 11`


## `Classes`
```
.className()
.classType()
.replace()
.toggle()
.array.from()
.classList
```
```
const littleColors = document.querySelectorAll('.palette-color')
let littleColorsArray = Array.from(littleColors)
const littleColorsArrayList = littleColorsArray.classList

for( const eachColor of littleColorsArray){
    eachColor.addEventListener('click', function(event) {
    classes.replace(classes[1] ,eachColor.classList[1] )
})
}
```
---


## `Classes with EventListener`

* We can query the class and add event listener to that to manipulate the classes. 
* If we query a class that has more than one element, we can use querySelectAll and use a for loop or for each loop.
* an example for `for each loop` is as shown:
  
```
  for( const eachColor of littleColorsArray){
    
    eachColor.addEventListener('click', function(event) {

    classes.replace(classes[1] ,eachColor.classList[1] )
})
}
```

  * an example of regular for loop to change classes of list of divs: 

```
for (let i = 0; i < newSquares.length; i++) {
    newSquares[i].addEventListener("click", function(event) {
        newSquares[i].classList.replace(newSquares[i].classList[1], classes[1])

    })
    }

```

```
function changeDoubleD6RollPics (){
    let roll = getRandomNumber(6)
    let rollAgain = getRandomNumber(6)
    doubleSixes.push(roll+rollAgain)

    document.querySelector('#double-d6-roll-1').src=`./images/d6/${roll}.png`
    document.querySelector('#double-d6-roll-2').src=`./images/d6/${rollAgain}.png`
    document.querySelector('#double-d6-rolls-mean').innerText = mean (doubleSixes).toFixed(2)
    document.querySelector('#double-d6-rolls-median').innerText = median (doubleSixes).toFixed(2)

}
```
---
## `Functions stored in variable`
```
const subtract = function (x,y) {
    return x-y
}

const add = function (x,y) {
    return x + y
}
```
```
const crazify = function(str) {
let newStr = ''
let count = 0
  for (let i = 0 ; i<str.length; i++) {
    if (str[i] === ' ' ) {
      newStr += ' '
      }
    else if (count % 2 === 0) {
        newStr += str[i].toLowerCase()
        count++
    } else  {
        newStr +=str[i].toUpperCase()
        count++
      }
    }
    return newStr
  }
```

---
## `Objects`
* We can use objectName.property for objects. 
```
function getFirstName(person) {
  return person.firstName;
}

function getLastName(person) {
  return person.lastName;
}

function getFullName(person) {
  return person.firstName + ' ' + person.lastName;
}
```
* We can also use loops with objects.

```
function giveBirthday(person) {
  
    if (person.age === undefined) {
      return person.age = 1
    } else {
      person.age = person.age + 1
    }
  }


function marry(person1, person2) {
person1.married = true
person2.married = true
person1.spouseName = person2.firstName + ' ' + person2.lastName
person2.spouseName = person1.firstName + ' ' + person1.lastName
}


function divorce(person1, person2) {
  person1.married = false
  person2.married = false
  delete person1.spouseName
  delete person2.spouseName
}
```
---