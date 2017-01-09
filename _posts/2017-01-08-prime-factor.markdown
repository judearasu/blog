---
layout: post
title:  "Determine the prime factor of a given number"
date:   2017-01-08 22:01:56 -0400 
categories: dsa
---
In this post, i tried with finding the prime factors.
For more clarity and explanation look into https://www.khanacademy.org/math/pre-algebra/pre-algebra-factors-multiples/pre-algebra-prime-factorization-prealg/v/prime-factorization

```javascript
var primeFactors = (function() {
  var primes = [];
  return {
    getPrimeFactors: getPrimeFactors
  };

  function getPrimeFactors(val){
    var i =2;
    var primeFactors = [];
    while(val > 2){
      if(val % i === 0){
        val = val/i;
        primeFactors.push(i);
      }else{
        i++;
      }
    }
    return primeFactors;
  }
})();
```
* [SourceCode](https://github.com/judearasu/dsa/blob/master/basics/primeFactors.js "PrimeFactors")
* [TestCoverage](https://github.com/judearasu/dsa/blob/master/tests/primeFactors.spec.js "PrimeFactorsSpec")
