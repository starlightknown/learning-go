# basic types
machive vs interpreted

`a=6` a is an object in interpreter and uses hardware - interpreted lang
`a :=6` a is not number/string - it is memory location - in go(machine lang)

int is the default type for intergers in Go, even lenghts
 non integers:
 - float32, float64 (not very accurate with divisions)
 - complex64, complex128
 - don't use floating point for money calculations, use a package instead.
 
 declarations
  anywhere:
  `var a int
  var (
  b=2
  f= 2.01
  )`
  
  only inside functions:
  `c := 2` (short declaration operator)
  
  %T - is used to show type of a value
  %v - used to show the value
  "_," (underscore comma) is used as a blank identifier, which is a way to discard values returned from functions or expressions that you don't intend to use.
  can be used for debugging in print statements
  
  %8T - number before used for space
  %[1]v - [1] says to reuse whatever parameter one was, so that we don't have to write again
  
  go is strict with types can't do a=b if types are different, we can do a=int(b)
  
  Special types:
  - bool : true or false, not convertible to/from intergers
  - error: Error() function, we can print it out, it can be nil or non nil
  - pointers : they are addresses, reference to something, may be nil or not
  
  Initializations: (go prevents the program by picking up some random memory address and assigns zero to everthing as initial value
  - All number types get 0 by default and initializes it
  - bool is false
  -  empty string or no chars
  -  everything gets nil
 
 Constants:
 Immutable!
 to be safe
 go limits const to numbers, strings, boolens
 type gets picks up with what it is initialized with
  
  # Strings
  
  strings in go are all unicode
  rune is go equivilent. of a charecter - 32bit
  utf-8 encoding unicode charecters
  byte - unit8
  ascii charecters fit into range 0-127
  len of string is the len of byte string to encode the string in utf8
  to deal with memory, bytes of the string
  string descriptor describes something, has pointer within and has memory location
  s := "hello world"
end of string is null bite
s += "es" makes a new memory and adds es to the s as strings are immutatble
s = strings.ToUpper(s)

# Arryas, Slices and maps

arrays are fixed size
gets copied
elements gets copied, there's no descriptor
comparable
if sizes are not same, once cant be assigned to other

slice is like array but string like - has a descriptor
slices can be changed - has variable lenghth and capacity
append takes a sclice and element and adds element to the slice
modify the slice descriptor and adds more space if used already
not comparable
cant be used as map key
has append and copy
e := a if we change e , a will change too
slces are indexed like [8:11]
8 is included 11 is not

