# javascript

// Create a program that takes user input and prints it to the console.
const user = prompt("Enter your name: ").trim()
if (user) {
    console.log(`Hello, ${user}!`)
} else {
    console.log("I don't get your name.")
}

// Write a function to check if a number is even or odd.
const input = prompt("Enter a number: ").trim();
const num = Number(input);

if (!isNaN(num)) {
    if (Math.abs(num % 2) === 1) {
        console.log("Odd number");
    } else {
        console.log("Even number");
    }
} else {
    console.log("Please provide a valid number.");
}


// Implement a function that reverses a string.

function StringRev(string){
    const reverse=string.split('').reverse().join('')
    console.log(`The reversed String ${reverse}`)
}

const input=prompt('Enter a string: ').trim()
if (input){
    StringRev(input)
}
else{
    console.log("Oops! I dont get any string")
}

// Create a simple calculator with addition, subtraction, multiplication, and division.
function calculator(num1,num2,operator){
    try{
        let result;
        switch(operator){
            case '+':
                result=num1+num2
                break
            case '-':
                result=num1-num2
                break
            case '*':
                result=num1*num2
                break
            case '/':
                if (num2===0) throw "Error: Division by Zero is not allowed"
                result=num1/num2
                break
            default:
                console.log("Invalid Operator!")
        }
    console.log(`Result ${result}`)
    } catch(error){
        console.log("Error")
    }
}

const num1=prompt("Enter value for num 1: ");
const num2=prompt("Enter value for num 2: ");
const operator=prompt("Enter valid operator + - * /")

calculator(num1,num2,operator)
