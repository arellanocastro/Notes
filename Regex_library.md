### WORD BOUNDARY
```
\bword\b
```

#### SUBSTITUTIONS
```
re.sub(r'(random)(pattern)', r'\desired outcome', str_to_analyse)
```

#### SUBSITUTIONS WITH FLAGS
```
re.sub(r'(random)(pattern)', r'\desired outcome', str_to_match, flags=re.IGNORECASE)
```

##### FOR 'desired outcome': THE NUMBERS REPRESENT THE GROUPS WITHIN (random)(pattern), WHERE (random) IS 1 AND (pattern) IS 2. 
```
r'\1 \3 \4 \5'
```

##### MATCH ANY(+) TEXT LENGTH 
```
[a-zA-Z]+
```

##### MATCH ANY TEXT, ACCENTED LETTERS(À-ú), NUMBERS(0-9) AND SPACES(\s) TOGETHER
```
[A-zÀ-ú0-9\s]+
```

##### Match special digits (. , * ? / )
Note: The \ is used to cancel the regular meaning of a letter, symbol or special digit
```
\*
```

##### MATCH ANY(+) DIGIT LENGTH
```
\d+
```

##### Match a blank space
```
\s
```

##### MATCH 1 TO 3 DIGITS TOGETHER
```
\d{1,3}
```


##### COMPILE PATTERNS
###### input: the pattern TP is saved as a variable. This variable can then be called with .findall to return lists with elements that match the pattern.

```
pattern=re.compile('TP')
result=pattern.findall('TP Tutorialspoint TP')
print result
result2=pattern.findall('TP is most popular tutorials site of India')
print result2
```

###### output
```
['TP', 'TP']
['TP']
```

### Online library to pick from as we used them: 
https://www.codexpedia.com/regex/regex-symbol-list-and-regex-examples/
