# Anuar Sadykov
### Junior Developer

----------

### Contact Information

**Phone:** +7 776 012 08 02<br>
**E-mail:** suhanjer@gmail.com<br>
**Telegram:** @AnuarSadykov<br>

----------

### About Myself:
For very long time I was interested in programming. More than a year ago I came upon "CS50: Introduction to Computer Science". Since then I have been trying to learn programming and dedicated my free time to practicing as much as I could.

----------

### Education and courses:

* **CS50's Introduction to Computer Science** (Complete)<br>
* **CS50's Web Programming with Python and JavaScript** (Final project)<br>
* **JavaScript/Front-end 2021Q3** (Just started)<br>

----------

### Code Example:

**Reverse or rotate?**<br>

*The input is a string str of digits. Cut the string into chunks (a chunk here is a substring of the initial string) of size sz (ignore the last chunk if its size is less than sz).*

*If a chunk represents an integer such as the sum of the cubes of its digits is divisible by 2, reverse that chunk; otherwise rotate it to the left by one position. Put together these modified chunks and return the result as a string.*

```javascript
function revrot(str, sz) {
    let length = str.length;
    let numchunks = Math.floor(length/sz, 1);
    if (sz == 0) {
        return "";
    }
    if (numchunks == 0){
        return "";
    }
    let arr = []
    for (let i=0; i<numchunks; i++){
        arr[i] = str.slice(0, sz);
        str = str.slice(sz);
    }
    for (let i in arr) {
        let sum = 0;
        for (let j of arr[i]) {
            sum = sum + parseInt(j)**3;
        }
        if (sum % 2 == 0) {
            arr[i] = arr[i].split("").reverse().join("");
        }
        else {
            let ch = arr[i].split("");
            //console.log(ch);
            let first = ch[0];
            ch = ch.slice(1);
            ch.push(first);
            arr[i] = ch.join("");
        }
    }
    return (arr.join(""));
}
```

----------

### Languages:
* **English** - B2 (Epam Test)<br>
* **Turkish**<br>
* **Russian**<br>