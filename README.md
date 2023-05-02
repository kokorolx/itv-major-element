# itv-major-element
We are given an array of size n, and we are required to find the majority element. The majority element is the element that appears more than [ n/2 ] times.


```

const majorArray = (arr) => {
  const count = {}
  const arrayLength = arr.length

  for(const element of arr) {
    count[element] ??= 0;
    count[element] += 1;
    if (count[element] > arrayLength/2) {
      return element;
    }
  }

 return Object.entries(count).sort((x, y) => y[1] - x[1])[0][0];
}

```
