# NAAPIE
“Everything in the universe has a rhythm, everything dances.” 
With Naapie, it’s easy to find your desired moment musics or podcasts for every moment – on your phone, your computer, your tablet and more.

There are millions of tracks and episodes on Naapie. So whether you’re behind the wheel, working out, partying or relaxing, the right music or podcast is always at your fingertips. Choose what you want to listen to, or let Naapie surprise you.

You can also browse through the collections of friends, artists, and celebrities, and just sit back. You have to, take a deep breath. and allow the music to flow through you. Revel in it, allow yourself to awe. When you play allow the music to break your heart with its beauty

Soundtrack your life with Naapie. Stay connected and enjoy and.

## V1.0.0 Titanium-octopus (Date)
## Features
##### ● Music from different languages (Nepali, Hindi, English, Bhojpuri, Tamil)
##### ● Collection of tracks from available languages
##### ● Popular artists along with their biography details
##### ● Playlists with collection of trending, popular and 90's hits
##### ● List of trending songs with artists
##### ● Popular 90's collection songs with must played tracks
##### ● Latest music from available languages
##### ● Collection of popular tracks from different singers
##### ● Option to play and add in the queue for auto track playing

## Requirement
1. Node > 10.x.x
2. Postman

## Endpoint Details
### Problem 1
**Endpoint**: ```http://localhost:3000/api/v1/smart-eq/equation-evaluator```
**Request body** 
```
JSON FILE LOCATED AT 
<project_folder>/configuration/equationFile.json>
```
**Note**: You have to modify the file for changing the request body.

**Response**
```
{
    "equation": "1+(x*10)=21",
    "value": 2
}
```

### Problem 2 
**Endpoint**: ```http://localhost:3000/api/v1/smart-eq/best-beers-evaluator```
**Request body** 
```
{
    "orderNumber":122
}
```

**Response**
```
{
    "status": 200,
    "sumOfDivisorsList": 64,
    "sumOfSubsetList": 63,
    "status_message": "First condition is voilated"
}
```

## PROBLEM AND STATEMENT
### Problem 1
#### Equation Simplification
You will be given a JSON file as an input. This file will contain a equation in a structured format
like this:
```json{
"op": "equal",
"lhs": {
"op": "add",
"lhs": 1,
"rhs": {
"op": "multiply",
"lhs": "x",
"rhs": 10
}
},
"rhs": 21
}
```
This particular example represents this equation:
1 + (x * 10) = 21
Your goal is to:
1. Parse the JSON into a structured format, and write a function to pretty-print the parsed
equation, in a single line with brackets, like the below example. (You can use a JSON
parsing library)
1 + (x * 10) = 21
2. Transform the expression so that you have ‘x’ on one side, and all the operations on the
other side. In this example, a transformed expression can be: x = (21 − 1) / 10
You should then print this simplified expression
3. Bonus: Evaluate the expression on the other side and find the value of ‘x’.
For our input files, assume that ‘x’ is always solvable.
Notes:
● The operations possible are: add, subtract, multiply, divide, and equal
● Each operation will have a LHS and a RHS. The LHS / RHS of a operation can be:
○ another operation,
○ Or a fixed number,
○ Or a variable reference
● The input files will be limited to have the following characteristics:
○ Top level operation will always be ‘equal’
○ RHS will always be a fixed number
○ LHS can be complex. But there will only be a single variable reference (x) that
occurs somewhere in the LHS. All other leaf nodes will be fixed numbers.

### Problem 2 
Once upon a time there was a tavern with 1000 beer taps, numbered from 1 to 1000.
You were told by a mysterious stranger that the best beers are the one with the taps
whose number matches those 2 conditions:
1) The sum of divisors (including 1, but not the number itself) of the tap number is
greater than tap number itself
2) No subset of those divisors sums up to the tap number itself
The waiter is coming, what is your order?
For example:
- Number 12: the proper divisors are 1, 2, 3, 4 and 6. The sum is 1+2+3+4+6 = 16 which is
greater than 12 and matches the first condition. However, the subset 2+4+6=12 which
violates the second condition.
You can solve this challenge in any language of your choice. Please submit the tap
number(s) and the source code of your solution.
