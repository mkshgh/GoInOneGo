# LEARN GIT IN ONE GO

## RUN

```go
// Example
package main
import ("fmt")

func main() {
  fmt.Println("Hello World!")
}
```

- run the main.go in the given folder
`go run .`

- run the specific go in the folder
`go run main.go`

- build an exectuable for your os
build creates platform specific build which you can use
`go build main.go`

## COMMENTS

```go
// Single Line Comments

/*
 Multi Line Comments
*/ 
```

## VARIABLES

| var                                                              |                                                 :=                                                  |  Cool |
| ---------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------: | ----: |
| Can be used inside and outside of functions                      |                                  Can only be used inside functions                                  | $1600 |
| Variable declaration and value assignment can be done separately | Variable declaration and value assignment cannot be done separately (must be done in the same line) |   $12 |

- Single variables

```go
var a string
var b int
var c bool
var x float32 = 123.78
var y float32 = 3.4e+38
var x float64 = 1.7e+308
```

- Multiple variables

```go
var a, b, c, d int = 1, 3, 5, 7
var a, b = 6, "Hello"
c, d := 7, "World!"

```

- Block variables

```go
var (
     a int
     b int = 1
     c string = "hello"
   )
```

- Constants

```go
// Constant names are usually written in uppercase letters 
const PI = 3.14

// Const with types
const A int = 1
```

## OUTPUTS

- Print and Println

```go
Print("prints in the same line")
Println("Prints in the new line")
```

- Printf

| Verb | Description |
|-------|:-------------:|
|%v| Prints the value in the default format|
|%#v| Prints the value in Go-syntax format|
|%T| Prints the type of the value|
|%%| Prints the % sign|

```go
  var i = 15.5
  var txt = "Hello World!"

  fmt.Printf("%v\n", i)
  fmt.Printf("%#v\n", i)
  fmt.Printf("%v%%\n", i)
  fmt.Printf("%T\n", i)

  fmt.Printf("%v\n", txt)
  fmt.Printf("%#v\n", txt)
  fmt.Printf("%T\n", txt)

    //Output
    //15.5
    //15.5
    //15.5%
    //float64
    //Hello World!
    //"Hello World!"
    //string
```

## INTEGERS VERB

|Verb| Description|
|----|:------------:|
|%b| Base 2|
|%d| Base 10|
|%+d| Base 10 and always show sign
|%o Base 8|
|%O| Base 8, with leading 0o|
|%x Base 16, lowercase|
|%X| Base 16, uppercase|
|%#x| Base 16, with leading 0x|
|%4d| Pad with spaces (width 4, right justified)|
|%-4d| Pad with spaces (width 4, left justified)|
|%04d| Pad with zeroes (width 4|

```go

  fmt.Printf("%b\n", i)
  fmt.Printf("%d\n", i)
  fmt.Printf("%+d\n", i)
  fmt.Printf("%o\n", i)
  fmt.Printf("%O\n", i)
  fmt.Printf("%x\n", i)
  fmt.Printf("%X\n", i)
  fmt.Printf("%#x\n", i)
  fmt.Printf("%4d\n", i)
  fmt.Printf("%-4d\n", i)
  fmt.Printf("%04d\n", i)

    //OUTPUT
    //1111
    //15
    //+15
    //17
    //0o17
    //f
    //F
    //0xf
    //  15
    //15
    //0015

```

## BASIC DATATYPES

### BOOL (true|false)

### INTEGERS

- UnSigned

| Type    | Size                                                                              | Range                                                                                                              |
| ------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
|  |
| `int`   | Depends on platform:<br>32 bits in 32 bit systems and<br>64 bit in 64 bit systems | \-2147483648 to 2147483647 in 32 bit systems and<br>\-9223372036854775808 to 9223372036854775807 in 64 bit systems |
| `int8`  | 8 bits/1 byte                                                                     | \-128 to 127                                                                                                       |
| `int16` | 16 bits/2 byte                                                                    | \-32768 to 32767                                                                                                   |
| `int32` | 32 bits/4 byte                                                                    | \-2147483648 to 2147483647                                                                                         |
| `int64` | 64 bits/8 byte                                                                    | \-9223372036854775808 to 9223372036854775807                                                                       |

- Unsigned

| Type| Size| Range|
| -------- | -------- | -------- |
|  |
| `uint`   | Depends on platform:<br>32 bits in 32 bit systems and<br>64 bit in 64 bit systems | 0 to 4294967295 in 32 bit systems and<br>0 to 18446744073709551615 in 64 bit systems |
| `uint8`  | 8 bits/1 byte                                                                     | 0 to 255                                                                             |
| `uint16` | 16 bits/2 byte                                                                    | 0 to 65535                                                                           |
| `uint32` | 32 bits/4 byte                                                                    | 0 to 4294967295                                                                      |
| `uint64` | 64 bits/8 byte                                                                    | 0 to 18446744073709551615                                                            |

### FLOAT

| Type      | Size    | Range                    |
| --------- | ------- | ------------------------ |
|  |
| `float32` | 32 bits | \-3.4e+38 to 3.4e+38.    |
| `float64` | 64 bits | \-1.7e+308 to +1.7e+308. |

### STRING

- The string data type is used to store a sequence of characters (text). String values must be surrounded by double quotes.

## SPECIAL DATATYPES

### Arrays

```go
var array_name = [length]datatype{values} // here length is defined
array_name := [length]datatype{values} // here length is defined

or

var array_name = [...]datatype{values} // here length is inferred
array_name := [...]datatype{values} // here length is inferred
```

```go
var arr1 = [3]int{1,2,3}
arr2 := [5]int{4,5,6,7,8}
var arr3 = [...]int{1,2,3}
arr4 := [...]int{4,5,6,7,8}
slice1 := arr2[2:4]
slice2 := arr1[1:3]
len(slice1)
cap(slice1)
append(myslice1, 20, 21)
append(slice1,slice2)
copy(dest, src)
[1 2 3]
[4 5 6 7 8]
[1 2 3]
[4 5 6 7 8]
[6 7]
2
4
[6 7 20 21]
[6 7 1,2,3]
```

## CONDITIONS

```go
if x > y {
   ...
  }
----------------------------------------
if condition {
  // code to be executed if condition is true
} else {
  // code to be executed if condition is false
}

----------------------------------------
if condition1 {
   // code to be executed if condition1 is true
} else if condition2 {
   // code to be executed if condition1 is false and condition2 is true
} else {
   // code to be executed if condition1 and condition2 are both false
}
---------------------------------------
if condition1 {
   // code to be executed if condition1 is true
  if condition2 {
     // code to be executed if both condition1 and condition2 are true
  }
}

```

## Switch

```go
switch expression {
case x:
   // code block
case y:
   // code block
case z:
...
default:
   // code block
}
-----------------
  day := 4

  switch day {
  case 1:
    fmt.Println("Monday")
  case 2:
    fmt.Println("Tuesday")
  case 3:
    fmt.Println("Wednesday")
  case 4:
    fmt.Println("Thursday")
  case 5:
    fmt.Println("Friday")
  case 6:
    fmt.Println("Saturday")
  case 7:
    fmt.Println("Sunday")
  }
--------------------
Multiple

switch expression {
case x,y:
   // code block if expression is evaluated to x or y
case v,w:
   // code block if expression is evaluated to v or w
case z:
...
default:
   // code block if expression is not found in any cases
}

-----------------------
   day := 5

   switch day {
   case 1,3,5:
    fmt.Println("Odd weekday")
   case 2,4:
     fmt.Println("Even weekday")
   case 6,7:
    fmt.Println("Weekend")
  default:
    fmt.Println("Invalid day of day number")
  }

```

## LOOPS

```go
for statement1; statement2; statement3 {
   // code to be executed for each iteration
}
-----------------------------------
  for i:=0; i < 5; i++ {
    fmt.Println(i)
  }
-----------------------------------
```

## Functions

```go
package main
import ("fmt")

func FunctionName() {
  fmt.Println("I just got excited!")
}

func main() {
  myMessage()
  myMessage()
  myMessage()
}

--------Parameters-----------
func familyName(fname string) {
  fmt.Println("Hello", fname, "LRufy")
}

func main() {
  familyName("mkshgh")
  familyName("KZoro")
  familyName("INami")
}

------RETURN------------

func myFunction(x int, y int) int {
  return x + y
}

func main() {
  fmt.Println(myFunction(1, 2))
}

--------RECURSION-----------
func testcount(x int) int {
  if x == 11 {
    return 0
  }
  fmt.Println(x)
  return testcount(x + 1)
}

func main(){
  testcount(1)
}
```

## STRUCT

A struct (short for structure) is used to create a collection of members of different data types, into a single variable.


```go
type Person struct {
  name string
  age int
  job string
  salary int
}

func main() {
  var pers1 Person
  var pers2 Person

  // Pers1 specification
  pers1.name = "Hege"
  pers1.age = 45
  pers1.job = "Teacher"
  pers1.salary = 6000

  // Pers2 specification
  pers2.name = "Cecilie"
  pers2.age = 24
  pers2.job = "Marketing"
  pers2.salary = 4500

  // Access and print Pers1 info
  fmt.Println("Name: ", pers1.name)
  fmt.Println("Age: ", pers1.age)
  fmt.Println("Job: ", pers1.job)
  fmt.Println("Salary: ", pers1.salary)

  // Access and print Pers2 info
  fmt.Println("Name: ", pers2.name)
  fmt.Println("Age: ", pers2.age)
  fmt.Println("Job: ", pers2.job)
  fmt.Println("Salary: ", pers2.salary)
}
-------STRUCT AS AN ARGUMENT------------------
type Person struct {
  name string
  age int
  job string
  salary int
}

func main() {
  var pers1 Person
  var pers2 Person

  // Pers1 specification
  pers1.name = "Hege"
  pers1.age = 45
  pers1.job = "Teacher"
  pers1.salary = 6000

  // Pers2 specification
  pers2.name = "Cecilie"
  pers2.age = 24
  pers2.job = "Marketing"
  pers2.salary = 4500

  // Print Pers1 info by calling a function
  printPerson(pers1)

  // Print Pers2 info by calling a function
  printPerson(pers2)
}

func printPerson(pers Person) {
  fmt.Println("Name: ", pers.name)
  fmt.Println("Age: ", pers.age)
  fmt.Println("Job: ", pers.job)
  fmt.Println("Salary: ", pers.salary)
}
```

## MAPS

KEY-VALUE PAIR

```go
--------SYNTAX----------
var a = map[KeyType]ValueType{key1:value1, key2:value2,...}

b := map[KeyType]ValueType{key1:value1, key2:value2,...}

---------EXAMPLE----------
var a = map[string]string{"brand": "Ford", "model": "Mustang", "year": "1964"}

b := map[string]int{"Oslo": 1, "Bergen": 2, "Trondheim": 3, "Stavanger": 4}

```

# REFERENCES
- https://go.dev/doc/
- https://www.w3schools.com/go/index.php
