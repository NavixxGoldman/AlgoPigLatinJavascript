# AlgoPigLatinJavascript
This is an algorithm to do the Pig Latin Challenge

```javascript
function translatePigLatin(str) {
 
  let regexVowel,pigLatin;
  //Regex Vowel 
  regexVowel=/[aeiou]/gi;


  if (str[0].match(regexVowel)){
      pigLatin= str+"way";
      return pigLatin;
  } else if (str.match(regexVowel)==null){
      pigLatin= str+"ay";
      return pigLatin;
  }else {
     var indiceVowel=str.indexOf(str.match(regexVowel)[0]);
     pigLatin= str.substring(indiceVowel)+str.substring(0,indiceVowel)+"ay";
     return pigLatin;

  }

  
}

console.log(translatePigLatin("glove"));
console.log(translatePigLatin("eight"));

```
