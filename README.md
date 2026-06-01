# Q9 - Count the Number of Words in a Paragraph

## Problem Statement

Write a JavaScript function to count the number of words present in a paragraph.

### Example

Input:

```javascript
const paragraph = "I am a HashedBit student";
```

Output:

```javascript
5
```

---

## Solution

```javascript
function countWords(paragraph) {
    return paragraph.trim().split(/\s+/).length;
}

const paragraph = "I am a HashedBit student";
console.log(countWords(paragraph));
```

---

## Explanation

### Step 1: Remove Extra Spaces

The `trim()` method removes spaces from the beginning and end of the string.

```javascript
paragraph.trim()
```

Example:

```javascript
"  Hello World  "
```

becomes

```javascript
"Hello World"
```

---

### Step 2: Split the Paragraph into Words

The `split(/\s+/)` method splits the string wherever one or more spaces occur.

```javascript
paragraph.split(/\s+/)
```

Example:

```javascript
"I am a HashedBit student"
```

becomes

```javascript
["I", "am", "a", "HashedBit", "student"]
```

---

### Step 3: Count the Words

The `length` property gives the total number of elements in the array.

```javascript
array.length
```

Result:

```javascript
5
```

---

## Dry Run

Input:

```javascript
"I am learning JavaScript today"
```

After split:

```javascript
["I", "am", "learning", "JavaScript", "today"]
```

Count:

```javascript
5
```

---

## Output

```javascript
5
```

---

## Alternative Solution Using reduce()

```javascript
function countWords(paragraph) {
    return paragraph
        .trim()
        .split(/\s+/)
        .reduce((count) => count + 1, 0);
}

console.log(countWords("I am a HashedBit student"));
```

---

## Conclusion

The function counts the number of words in a paragraph by:

1. Removing extra spaces.
2. Splitting the text into words.
3. Returning the total number of words.

Time Complexity: **O(n)**

where **n** is the length of the paragraph.
