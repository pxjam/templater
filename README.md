# HTML templater

includes, loops etc

## Examples
https://github.com/TheColorRed/node-tpl
https://github.com/ecomfe/smarty4js/

### Smaple syntax

### Simple file include

`[-tpl/item.html-]`

### Loop file include with json context

```
[-tpl/item.html, [{
    name: 'Коля',
    age: 28
},{
    name: 'Коля',
    age: 28
}]-]
```

### Placeholders

```
[-title-]
[-person.name-]
```

### Set variable
```
[-set items = [{
    name: 'Коля',
    age: 28
},{
    name: 'Коля',
    age: 28
}]-]
```

### Inline for each loop
```
[-each items-]
    <li>
        [-name-]: [-age-]
    </li>
[-/each-]
```
```
[-each [{
   name: 'Коля',
   age: 28
},{
   name: 'Коля',
   age: 28
}]-]
    <li>
        [-name-]: [-age-]
    </li>
[-/each-]
```

### If statement
```
[-if person-]
    <li>Hello, [-person!-]</li>
[-/if-]
```
