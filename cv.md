# Ilya Lubchonak

## Contact Information
* Email: Sindiano@yandex.ru
* Phone: +375(25)750-69-36
* GitHub: Sindiano

## Brief Self-Introduction


## Skills
* C#
* SQL
* HTML
* CSS
* JS

## Code Examples

*(Solution to [Kata](https://www.codewars.com/kata/521c2db8ddc89b9b7a0000c1 "Snail") on CodeWars)*

```JavaScript

const Directions = [
  [0,1],      //right
  [1,0],      //down
  [0,-1],     //left
  [-1,0]      //up
];

check = function(array,iPos,jPos,checkDI){
  iPos = iPos+Directions[checkDI][0];
  jPos = jPos+Directions[checkDI][1];
  if (
    iPos == -1 ||
    iPos == array[0].length ||
    jPos == -1 ||
    jPos == array[0].length )
     return false
    else return array[iPos][jPos] != -1;
}

snail = function(array) {
  if(array[0].length  == 0) return [];
  let   n = array[0].length, 
        ic = Math.floor(n / 2),
        jc = Math.floor(n/2) - (n%2==0?1:0);
  let i = 0, j = 0, di = 0, res = [];
  while (check(array,i,j,(di+1)%4)){
      res.push(array[i][j]);
      array[i][j] = -1;
      if (check(array,i,j,di)){
        i = i+Directions[di][0];
        j = j+Directions[di][1];
      } else {
        di = (di+1)%4;
        i = i+Directions[di][0];
        j = j+Directions[di][1];
      }
    }
  res.push(array[ic][jc]);
  return res;
}
```

## Work Experience

## Education

Belarusian State Technological University,

Information Technology Faculty,

Department of Software Engineering (didn't finish, 3 years)

## English Language

Proficiency level: B2