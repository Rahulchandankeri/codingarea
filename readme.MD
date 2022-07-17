# CODING QUESTIONS

### Table of Contents

| No. | Questions                                                                                                                                                       |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Capitalize the first letter of the word](#capitalize-the-first-letter-of-the-word)                                                                             |
| 2   | [Write a program to check the palindrome of a string](#write-a-program-to-check-the-palindrome-of-a-string)                                                     |
| 3   | [Reverse a string](#reverse-a-string)                                                                                                                           |
| 4   | [Write a program to find un-common string in output1 and output2 and viceversa](#write-a-program-to-find-un-common-string-in-output1-and-output2-and-viceversa) |
| 5   | [Program to find Vowel Count](#program-to-find-vowel-count)                                                                                                     |
| 6   | [Grasshopper Grade book](#grasshopper-grade-book)                                                                                                               |
| 7   | [Count of positive sum of negatives](#count-of-positive-sum-of-negatives)                                                                                       |

1. ## Capitalize the first letter of the word

```const capitalizeFirstLetter = (str) => {
str = str.split(" ");
 let cap;
 let arr =[]
for(let i=0; i<str.length; i++) {
str[i] = str[i][0].toUpperCase() +str[i].substr(1);
}
 str = str.join(" ");
 console.log(str)
}
capitalizeFirstLetter("i am going to mumbai")
```

**[⬆ Back to Top](#table-of-contents)**

#

2. ## Write a program to check the palindrome of a string

```
// Check whether a String is Palindrome or not
	const isPalindrome =  str => {
	let revStr =  str.split("").reverse().join("");
	revStr === str ? console.log(`${str} is palindrome`) : console.log(`${str} is not a palindrome`);
	return revStr
	}


	isPalindrome("abba")
```

**[⬆ Back to Top](#table-of-contents)**

#

3.  ### Reverse a string

```
// Reverse a string
const reverseString = (str) => {
str = str.split(" ").reverse().join(" ")
console.log(str)
return str
}
reverseString("rahul is going");
```

**[⬆ Back to Top](#table-of-contents)**

#

4. ### Write a program to find un-common string in output1 and output2 and viceversa

```
   const uncommonStr = (str1, str2) => {
   let output1 = "";
   let output2 = "";

for(let i =0; i< str1.length; i++) {
if(str2.indexOf(str1[i]) === -1) {
output1 += str1[i]
}
}
for(let j =0; j<str2.length; j++) {
if(str1.indexOf(str2[j]) === -1) {
output2 += str2[j]
}
}
console.log(output1, output2)
}
uncommonStr("BC", "BANGALORE")
```

**[⬆ Back to Top](#table-of-contents)**

#

5. ### Program to find Vowel Count

```
function getCount(str) {
  var vowelsCount = 0;
  var vowels = ["a","e","i","o","u"];
  for(var i = 0;i < str.length;i++){
    for(var j=0;j<vowels.length;j++){
      if(str[i] === vowels[j]){
        vowelsCount++;
      }
    }
  }
  console.log(vowelsCount)
  return vowelsCount;
}
getCount("abracadabra");
```

[LIVE](https://jsfiddle.net/rahulchandankeri/umx2dcg1/4/)

**[⬆ Back to Top](#table-of-contents)**

#

6. ### Grasshopper Grade book

```
// Grasshopper Grade book
function getGrade (s1, s2, s3) {
// Code here
const averageScore = +((s1 + s2 + s3) / 3).toFixed(2);

if(averageScore >= 90 && averageScore <= 100) return "A";
if(averageScore >= 80 && averageScore < 90) return "B";
if(averageScore >= 70 && averageScore < 80) return "C";
if(averageScore >= 60 && averageScore < 70) return "D";
if(averageScore >= 0 && averageScore < 60) return "F";
}
```

[LIVE](https://jsfiddle.net/rahulchandankeri/wnkar12h/23/)

**[⬆ Back to Top](#table-of-contents)**

#

#### Q7

### Count of positive sum of negatives

### More Explantion:

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.
If the input is an empty array or is null, return an empty array.

Example:
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

### Code:

```
//Count of positives / sum of negatives
function countPositivesSumNegatives(input) {
    if (input == null || input.length == 0)
      return [];

  // your code here
    let countOfPositive = 0;
     let sumOfNegative = 0;


  for(let i =0; i<input.length; i++) {

     if(input[i] > 0  ) {
       countOfPositive++ ;
     }
 else
      sumOfNegative += input[i];

   }

   console.log([countOfPositive, sumOfNegative])
   return [countOfPositive  , sumOfNegative]


}


countPositivesSumNegatives([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15])
countPositivesSumNegatives([0, 2, 3, 0, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14])

```

[LIVE](https://jsfiddle.net/rahulchandankeri/ja37f9Lm/14/)

**[⬆ Back to Top](#table-of-contents)**

#
