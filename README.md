# CodeCadmy Rock, Paper, or Scissors Solution/Implementation

var userInput = 'Rock';
userInput = userInput.toLowerCase();  //change tha input into lower case 

function getComputerChoice() {
   var randomNumber = Math.floor(Math.random() * 3); //create random number from  0 to 2
   switch(randomNumber) {
    case 0:
        return 'rock';
        break;
    case 1:
        return 'paper';
        break;
     case 2:
        return 'scissors';
        break;
       }
}

function determineWinner(userChoice,computerChoice) 
{
  //Condition for Cheat code
  if (userChoice === 'bomb')  {
    return 'You win by cheat code';
  }
  
  //When choices are same 
  else if (userChoice === computerChoice) {
    return 'Game Tie';
  }

  else if (userChoice === 'rock') {
     if (computerChoice === 'paper') {
       return 'Computer is Winner';
     }
     else  {
       return 'User is  Winner';
     }    
  }
  
   else if (userChoice === 'paper') {
     if (computerChoice === 'scissors') {
       return 'Computer is Winner';
     }
     else  {
      return 'User is  Winner';
     }    
  }  
  
  else if (userChoice === 'scissors') {
     if (computerChoice === 'rock') {
       return 'Computer is Winner';
     }
     else  {
       return 'User is  Winner';
     }    
   }  
}
console.log(determineWinner('bomb',getComputerChoice()));  //to demonstrate cheatcode condition
