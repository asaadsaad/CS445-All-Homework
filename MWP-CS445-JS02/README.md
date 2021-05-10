# MWP - CS445 - JavaScript 02
## Exercise 01

Complete the code for the `ImmutableStorage` class that will override `setItem()` to work with an immutable `Storage` object.
```typescript
type Obj = { [key: string]: string };

class MyStorage {
    private storage: Obj = {};

    getItem(key: string): string {
        return this.storage[key]
    }
    setItem(key: string, value: string): void {
        this.storage[key] = value
    }
    getStorage(): Obj {
        return this.storage;
    }
}

class ImmutableStorage extends MyStorage {
    constructor() {
        super();
        Object.freeze(this.storage);
    }
    // complete the code here
}
```
  
## Exercise 02
Write a function `function removeDuplicates(): number[] {}` that will work on any `Array` object, the function will remove all the duplicate numbers from an array. 
```typescript
[4, 1, 5, 7, 2, 3, 1, 4, 6, 5, 2].removeDuplicates(); 

// returns: [4, 1, 5, 7, 2, 3, 6]
```
  
## Exercise 03
Write a function `filterWords(string[]): string {}` that will work on any `String` object. It accepts an array of strings that specifies a list of banned words. The function returns the string after replacing all the banned words with three stars.
```javascript
console.log("This course is awesome".filterWords(['course', 'awesome'])); 
   
//"This *** is ***"
```
