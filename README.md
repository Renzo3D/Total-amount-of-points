# Total-amount-of-points

Kata of the Day Total amount of points


In this kata we have to add the total amount of points of ten games. 

game Won = +3 points, 

Draw game = +1 point, 

loss = 0 points. 

We will be giving an array of 10 scores of two teams. team A and team B, Being team A the team we will count points of. 

If the first game == Array[0] has 2:0; that means the first game team A WON '2' - '0' against team B;  we would add 3 points to total points.


If the first game == Array[0] has 0:2; that means the first game team A LOSS '0' - '2' against team B; We don't add 1 points. 


If the first game == Array[0] has 2:2; that means the first game team A DRAW '2' - '2' against team B; We would add 1 point to total points.


Now with this gold in mind lets start doing some coding.


So we have an Array of size 10, BUT in each Index there are two values, value A and value B, these values represent the scoe of each game.


Example Testing for points(['1:0','2:0','3:0','4:0','2:1','3:1','4:1','3:2','4:2','4:3'])


If we see the first array we see the follow. Array[0] = '1:0' 


inside array[0] there are 3 index being index[0] = '1'; index[1] = ':' ; index[2] = '0'; // 3 index starting from 0. 


all we need to compare is index[0] ande index[2];

this is how you compare if index[0] is grater||equal||less than index[2] of array[0] 


array[0][0] > array[0][2];   


array[0][0] == array[0][2];


array[0][0] < array[0][2];


Now Lest do the final code. 


function points(games) {

var result = 0;                      // we initialize the value of result zero

for(var i=0; i < 10; i ++){          // we know that there are 10 games so we count from 0 to 9 (btw 0 and 9 there are 10 digits)
  
  if(games[i][0] > games[i][2])      // We hardcode the index[0] and [2] because those are always going to be the values to compare. 
  
   result = result + 3;              // here we add 3 to result.
   
   if(games[i][0] == games[i][2])
    
   result = result + 1;              // here we add 1 to result.
  
  }
  
  return result;                     // result ahs to be outside the loop and it keep getting update for each comparison that gets done
  
}



I hope this help you understand how this Kata works; 

if you have questions please just let me know. remember to ABC... Always Be Coding. 

