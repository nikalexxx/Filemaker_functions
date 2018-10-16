# Filemaker_functions
Useful custom functions for Filemaker

## Examples

### map_eval  
```javascript
map_eval(range(1;3);"e";"e*e") // "1¶4¶9"
map_eval("a¶b¶c";"e";"Char(Code(e)+10)") // "k¶l¶m"
```

### reduce_eval  
```javascript
reduce_eval(range(1;100);"a";"e";"a+e";0) // 5050 (sum)
reduce_eval(range(1;6);"a";"e";"a*e";1) // 720 (factorial)
reduce_eval(range(1;10);"a";"e";"a & \"@\"";"") // "@@@@@@@@@@"
```

### map
```javascript
map("a¶b¶c";"Upper") // "A¶B¶C"
map("-1¶2¶-3";"Abs") // "1¶2¶3"
```

### range
```javascript
range(1;3) // "1¶2¶3"
range(2;-2) // "2¶1¶0¶-1¶-2"
```

### array_include
```javascript
array_include("a¶b¶c";"a") // True
array_include("a¶b¶c";"d") // False
```

### H
```
Set Variable [ $var[H("value 1")] ; 1]
Set Variable [ $var[H("value 2")] ; 2]

Show Custom Dialog [ $var[H("value 1")] + $var[H("value 2")] ]
```
