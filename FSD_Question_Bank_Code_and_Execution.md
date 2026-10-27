# Full Stack Development Question Bank — Code and Execution Commands

Based on **FSD QB.pdf**. Each question includes the file name(s), complete code, and execution commands. Replace sample names, roll numbers, and database connection strings with your own values where necessary.

## General setup

- Install Node.js LTS and verify with `node -v` and `npm -v`.
- JavaScript files are run with `node filename.js`.
- React questions use Vite. Create a project with `npm create vite@latest fsd-react-practicals -- --template react`, then `cd fsd-react-practicals` and `npm install`.
- For React Router and Axios questions, install `npm install react-router-dom axios`.
- For Express questions, create a separate backend folder and run `npm init -y`, then install the packages specified for that question.
- For MongoDB shell commands, open `mongosh` while MongoDB is running.
- Where multiple questions use `src/App.jsx`, use the code for the question you are practising; each is a separate practical and replaces the previous `App.jsx`.

---

# Q.1 — A. JavaScript Programs

## 1. Demonstrate operators and control statements in JavaScript

**File:** `q1_01_operators_control.js`

```javascript
const a = 20;
const b = 6;

console.log("Arithmetic Operators");
console.log("Addition:", a + b);
console.log("Subtraction:", a - b);
console.log("Multiplication:", a * b);
console.log("Division:", a / b);
console.log("Remainder:", a % b);

console.log("Comparison Operators");
console.log("a > b:", a > b);
console.log("a === b:", a === b);

console.log("Logical Operators");
console.log("(a > 10 && b < 10):", a > 10 && b < 10);
console.log("(a < 10 || b < 10):", a < 10 || b < 10);

if (a > b) {
    console.log("a is greater than b");
} else {
    console.log("b is greater than or equal to a");
}

for (let i = 1; i <= 5; i++) {
    console.log("For loop:", i);
}

let count = 1;
while (count <= 3) {
    console.log("While loop:", count);
    count++;
}

switch (b) {
    case 6:
        console.log("The value of b is six");
        break;
    default:
        console.log("The value of b is not six");
}
```

**Execution:** `node q1_01_operators_control.js`

## 2. Print even numbers from 1 to 50

**File:** `q1_02_even_numbers.js`

```javascript
for (let number = 1; number <= 50; number++) {
    if (number % 2 === 0) {
        console.log(number);
    }
}
```

**Execution:** `node q1_02_even_numbers.js`

## 3. Declare variables and write a function to calculate the sum of two numbers

**File:** `q1_03_sum_function.js`

```javascript
let firstNumber = 25;
let secondNumber = 35;

function calculateSum(a, b) {
    return a + b;
}

const result = calculateSum(firstNumber, secondNumber);
console.log("First number:", firstNumber);
console.log("Second number:", secondNumber);
console.log("Sum:", result);
```

**Execution:** `node q1_03_sum_function.js`

## 4. Find the largest of three numbers

**File:** `q1_04_largest_number.js`

```javascript
const firstNumber = 45;
const secondNumber = 78;
const thirdNumber = 62;

let largest;

if (firstNumber >= secondNumber && firstNumber >= thirdNumber) {
    largest = firstNumber;
} else if (secondNumber >= firstNumber && secondNumber >= thirdNumber) {
    largest = secondNumber;
} else {
    largest = thirdNumber;
}

console.log("First number:", firstNumber);
console.log("Second number:", secondNumber);
console.log("Third number:", thirdNumber);
console.log("Largest number:", largest);
```

**Execution:** `node q1_04_largest_number.js`

## 5. Find factorial using a loop and template literals

**File:** `q1_05_factorial.js`

```javascript
const number = 5;
let factorial = 1;

if (number < 0) {
    console.log("Factorial is not defined for negative numbers.");
} else {
    for (let i = 1; i <= number; i++) {
        factorial = factorial * i;
    }
    console.log(`Factorial of ${number} is ${factorial}`);
}
```

**Execution:** `node q1_05_factorial.js`

## 6. Find the reverse of a number

**File:** `q1_06_reverse_number.js`

```javascript
let number = 12345;
let originalNumber = number;
let reverse = 0;

while (number > 0) {
    const digit = number % 10;
    reverse = reverse * 10 + digit;
    number = Math.floor(number / 10);
}

console.log("Original number:", originalNumber);
console.log("Reversed number:", reverse);
```

**Execution:** `node q1_06_reverse_number.js`

## 7. Implement arrays in JavaScript

**File:** `q1_07_arrays.js`

```javascript
const fruits = ["Apple", "Banana", "Mango", "Orange"];

console.log("Complete array:", fruits);
console.log("First fruit:", fruits[0]);
console.log("Array length:", fruits.length);

fruits.push("Grapes");
console.log("After push:", fruits);

fruits[1] = "Pineapple";
console.log("After updating second item:", fruits);

for (let index = 0; index < fruits.length; index++) {
    console.log(`Fruit at index ${index}: ${fruits[index]}`);
}
```

**Execution:** `node q1_07_arrays.js`

## 8. Demonstrate arrow functions

**File:** `q1_08_arrow_functions.js`

```javascript
const greet = () => {
    console.log("Welcome to JavaScript arrow functions.");
};

const square = (number) => {
    return number * number;
};

greet();
console.log("Square of 6:", square(6));
```

**Execution:** `node q1_08_arrow_functions.js`

## 9. Add two numbers using an arrow function

**File:** `q1_09_arrow_sum.js`

```javascript
const addNumbers = (firstNumber, secondNumber) => {
    return firstNumber + secondNumber;
};

const firstNumber = 12;
const secondNumber = 18;
const sum = addNumbers(firstNumber, secondNumber);

console.log(`${firstNumber} + ${secondNumber} = ${sum}`);
```

**Execution:** `node q1_09_arrow_sum.js`

## 10. Print a multiplication table using a loop and template literals

**File:** `q1_10_multiplication_table.js`

```javascript
const number = 7;

console.log(`Multiplication table of ${number}`);

for (let i = 1; i <= 10; i++) {
    console.log(`${number} x ${i} = ${number * i}`);
}
```

**Execution:** `node q1_10_multiplication_table.js`

## 11. Check even or odd using an arrow function

**File:** `q1_11_even_odd_arrow.js`

```javascript
const checkEvenOdd = (number) => {
    if (number % 2 === 0) {
        return "Even";
    }
    return "Odd";
};

const number = 17;
console.log(`${number} is ${checkEvenOdd(number)}`);
```

**Execution:** `node q1_11_even_odd_arrow.js`

## 12. Demonstrate arrays and objects

**File:** `q1_12_arrays_objects.js`

```javascript
const student = {
    name: "Aarav",
    rollNumber: 101,
    course: "BSc IT"
};

const subjects = ["JavaScript", "React", "Node.js"];

console.log("Student object:", student);
console.log("Student name:", student.name);
console.log("Subjects array:", subjects);

subjects.forEach((subject) => {
    console.log("Subject:", subject);
});
```

**Execution:** `node q1_12_arrays_objects.js`

## 13. Perform `map()`, `filter()` and `reduce()`

**File:** `q1_13_map_filter_reduce.js`

```javascript
const numbers = [1, 2, 3, 4, 5, 6];

const doubledNumbers = numbers.map((number) => {
    return number * 2;
});

const evenNumbers = numbers.filter((number) => {
    return number % 2 === 0;
});

const total = numbers.reduce((sum, number) => {
    return sum + number;
}, 0);

console.log("Original numbers:", numbers);
console.log("Numbers after map():", doubledNumbers);
console.log("Even numbers after filter():", evenNumbers);
console.log("Sum after reduce():", total);
```

**Execution:** `node q1_13_map_filter_reduce.js`

## 14. Create a student object and display its properties

**File:** `q1_14_student_object.js`

```javascript
const student = {
    name: "Harsh",
    rollNumber: "IT24011",
    course: "BSc Information Technology",
    semester: 5,
    college: "Your College Name"
};

console.log("Student Details");
console.log("Name:", student.name);
console.log("Roll Number:", student.rollNumber);
console.log("Course:", student.course);
console.log("Semester:", student.semester);
console.log("College:", student.college);
```

**Execution:** `node q1_14_student_object.js`

## 15. Store student details in an array of objects

**File:** `q1_15_students_array.js`

```javascript
const students = [
    { name: "Aarav", rollNumber: 101, course: "BSc IT" },
    { name: "Diya", rollNumber: 102, course: "BSc IT" },
    { name: "Kabir", rollNumber: 103, course: "BSc IT" }
];

console.log("Student Records");

students.forEach((student) => {
    console.log("-------------------------");
    console.log("Name:", student.name);
    console.log("Roll Number:", student.rollNumber);
    console.log("Course:", student.course);
});
```

**Execution:** `node q1_15_students_array.js`

## 16. Store student marks in an array of objects

**File:** `q1_16_student_marks.js`

```javascript
const students = [
    { name: "Aarav", marks: 82 },
    { name: "Diya", marks: 91 },
    { name: "Kabir", marks: 67 },
    { name: "Meera", marks: 76 }
];

students.forEach((student) => {
    console.log(`${student.name} scored ${student.marks} marks.`);
});
```

**Execution:** `node q1_16_student_marks.js`

## 17. Accept student marks and calculate percentage, grade and pass/distinction status

**File:** `q1_17_student_result.js`

```javascript
const prompt = require("prompt-sync")();

const studentName = prompt("Enter student name: ");
const subject1 = Number(prompt("Enter marks for subject 1 (out of 100): "));
const subject2 = Number(prompt("Enter marks for subject 2 (out of 100): "));
const subject3 = Number(prompt("Enter marks for subject 3 (out of 100): "));
const subject4 = Number(prompt("Enter marks for subject 4 (out of 100): "));
const subject5 = Number(prompt("Enter marks for subject 5 (out of 100): "));

const marks = [subject1, subject2, subject3, subject4, subject5];

if (marks.some((mark) => !Number.isFinite(mark) || mark < 0 || mark > 100)) {
    console.log("Invalid marks. Enter marks between 0 and 100.");
} else {
    const total = marks.reduce((sum, mark) => sum + mark, 0);
    const percentage = total / 5;
    let grade;

    if (percentage >= 75) {
        grade = "Distinction";
    } else if (percentage >= 60) {
        grade = "First Class";
    } else if (percentage >= 50) {
        grade = "Second Class";
    } else if (percentage >= 40) {
        grade = "Pass";
    } else {
        grade = "Fail";
    }

    const status = marks.every((mark) => mark >= 35) ? "Pass" : "Fail";

    console.log("Student Name:", studentName);
    console.log("Total Marks:", total, "out of 500");
    console.log("Percentage:", `${percentage.toFixed(2)}%`);
    console.log("Grade:", grade);
    console.log("Pass/Fail Status:", status);
    console.log("Distinction Status:", percentage >= 75 && status === "Pass" ? "Distinction" : "No Distinction");
}
```

**Execution:**
```bash
npm init -y
npm install prompt-sync
node q1_17_student_result.js
```

## 18. Calculate simple interest

**File:** `q1_18_simple_interest.js`

```javascript
function calculateSimpleInterest(principal, rate, time) {
    const simpleInterest = (principal * rate * time) / 100;
    return simpleInterest;
}

const principal = 10000;
const rate = 5;
const time = 2;
const interest = calculateSimpleInterest(principal, rate, time);

console.log("Principal:", principal);
console.log("Rate:", rate, "%");
console.log("Time:", time, "years");
console.log("Simple Interest:", interest);
console.log("Total Amount:", principal + interest);
```

**Execution:** `node q1_18_simple_interest.js`

## 19. Use `push()`, `pop()`, `shift()` and `unshift()`

**File:** `q1_19_array_methods.js`

```javascript
const products = ["Laptop", "Mobile", "Keyboard", "Mouse", "Monitor"];

console.log("Original products:", products);

products.push("Printer");
console.log("After push():", products);

const removedLastProduct = products.pop();
console.log("Removed by pop():", removedLastProduct);
console.log("After pop():", products);

const removedFirstProduct = products.shift();
console.log("Removed by shift():", removedFirstProduct);
console.log("After shift():", products);

products.unshift("Tablet");
console.log("After unshift():", products);
```

**Execution:** `node q1_19_array_methods.js`

## 20. Calculate square, cube and even/odd status

**File:** `q1_20_number_functions.js`

```javascript
function calculateSquare(number) {
    return number * number;
}

function calculateCube(number) {
    return number * number * number;
}

function checkEvenOdd(number) {
    if (number % 2 === 0) {
        return "Even";
    }
    return "Odd";
}

const number = 4;

console.log("Number:", number);
console.log("Square:", calculateSquare(number));
console.log("Cube:", calculateCube(number));
console.log("Even/Odd:", checkEvenOdd(number));
```

**Execution:** `node q1_20_number_functions.js`

## 21. Increase employee salaries by 10% using `map()` and filter them

**File:** `q1_21_employee_salaries.js`

```javascript
const salaries = [20000, 25000, 30000, 40000, 50000];

const increasedSalaries = salaries.map((salary) => {
    return salary * 1.10;
});

const salariesAbove30000 = increasedSalaries.filter((salary) => {
    return salary > 30000;
});

console.log("Original salaries:", salaries);
console.log("Salaries after 10% increase:", increasedSalaries);
console.log("Increased salaries above 30000:", salariesAbove30000);
```

**Execution:** `node q1_21_employee_salaries.js`

## 22. Library program to add, search and list available books

**File:** `q1_22_library.js`

```javascript
const books = [
    { id: 1, title: "The Alchemist", author: "Paulo Coelho", available: true },
    { id: 2, title: "Wings of Fire", author: "A. P. J. Abdul Kalam", available: true },
    { id: 3, title: "Atomic Habits", author: "James Clear", available: false }
];

function addBook(id, title, author) {
    const newBook = {
        id: id,
        title: title,
        author: author,
        available: true
    };
    books.push(newBook);
    console.log(`Book "${title}" added successfully.`);
}

function searchBook(title) {
    const book = books.find((item) => {
        return item.title.toLowerCase() === title.toLowerCase();
    });

    if (book) {
        console.log("Book found:", book);
    } else {
        console.log("Book not found.");
    }
}

function listAvailableBooks() {
    const availableBooks = books.filter((book) => {
        return book.available === true;
    });

    console.log("Available books:");
    availableBooks.forEach((book) => {
        console.log(`${book.id}. ${book.title} by ${book.author}`);
    });
}

addBook(4, "Deep Work", "Cal Newport");
searchBook("Atomic Habits");
listAvailableBooks();
```

**Execution:** `node q1_22_library.js`

## 23. Use `switch` for day name and ternary operator for leap year

**File:** `q1_23_switch_leap_year.js`

```javascript
const dayNumber = 3;
let dayName;

switch (dayNumber) {
    case 1:
        dayName = "Monday";
        break;
    case 2:
        dayName = "Tuesday";
        break;
    case 3:
        dayName = "Wednesday";
        break;
    case 4:
        dayName = "Thursday";
        break;
    case 5:
        dayName = "Friday";
        break;
    case 6:
        dayName = "Saturday";
        break;
    case 7:
        dayName = "Sunday";
        break;
    default:
        dayName = "Invalid day number";
}

console.log("Day:", dayName);

const year = 2024;
const leapYearMessage = (year % 400 === 0 || (year % 4 === 0 && year % 100 !== 0))
    ? `${year} is a leap year`
    : `${year} is not a leap year`;

console.log(leapYearMessage);
```

**Execution:** `node q1_23_switch_leap_year.js`

## 24. Print a star triangle and Fibonacci series

**File:** `q1_24_patterns_fibonacci.js`

```javascript
const rows = 5;

console.log("Star Triangle");
for (let i = 1; i <= rows; i++) {
    let pattern = "";
    for (let j = 1; j <= i; j++) {
        pattern += "* ";
    }
    console.log(pattern);
}

const terms = 10;
let first = 0;
let second = 1;

console.log("Fibonacci Series");
for (let i = 1; i <= terms; i++) {
    console.log(first);
    const next = first + second;
    first = second;
    second = next;
}
```

**Execution:** `node q1_24_patterns_fibonacci.js`

## 25. Convert Celsius to Fahrenheit and Fahrenheit to Celsius

**File:** `q1_25_temperature_converter.js`

```javascript
const celsiusToFahrenheit = (celsius) => {
    return (celsius * 9 / 5) + 32;
};

const fahrenheitToCelsius = (fahrenheit) => {
    return (fahrenheit - 32) * 5 / 9;
};

let celsius = 25;
let fahrenheit = 77;

console.log(`${celsius}°C = ${celsiusToFahrenheit(celsius).toFixed(2)}°F`);
console.log(`${fahrenheit}°F = ${fahrenheitToCelsius(fahrenheit).toFixed(2)}°C`);
```

**Execution:** `node q1_25_temperature_converter.js`

## 26. Calculate electricity bill using a default parameter and return value

**File:** `q1_26_electricity_bill.js`

```javascript
function calculateElectricityBill(units, rate = 7) {
    if (units < 0) {
        return "Units cannot be negative.";
    }

    const billAmount = units * rate;
    return billAmount;
}

const unitsConsumed = 150;
const bill = calculateElectricityBill(unitsConsumed);

console.log("Units consumed:", unitsConsumed);
console.log("Rate per unit: ₹7");
console.log("Electricity bill: ₹" + bill);
```

**Execution:** `node q1_26_electricity_bill.js`

---

# Q.1 — B. React Components, State and Forms

## React setup used for Questions 27–47

Run these commands once:

```bash
npm create vite@latest fsd-react-practicals -- --template react
cd fsd-react-practicals
npm install
npm run dev
```

For each question, create or replace the named files in `src/`. Vite uses the following entry point.

**File:** `src/main.jsx`

```jsx
import React from "react";
import { createRoot } from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

createRoot(document.getElementById("root")).render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);
```

**Execution:** `npm run dev`

## 27. Create a simple functional component and render it

**File:** `src/App.jsx`

```jsx
import React from "react";

function App() {
    return (
        <div>
            <h1>My First Functional Component</h1>
            <p>This component is rendered by React.</p>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 28. Functional component displaying a heading and paragraph

**File:** `src/App.jsx`

```jsx
import React from "react";

function HeadingParagraph() {
    return (
        <section>
            <h1>Full Stack Development</h1>
            <p>React is a JavaScript library used to build user interfaces.</p>
        </section>
    );
}

export default HeadingParagraph;
```

**Execution:** `npm run dev`

## 29. Functional component displaying a welcome message

**File:** `src/App.jsx`

```jsx
import React from "react";

function Welcome() {
    return (
        <div>
            <h1>Welcome to React</h1>
            <p>We are learning React functional components.</p>
        </div>
    );
}

export default Welcome;
```

**Execution:** `npm run dev`

## 30. Render multiple functional components on one page

**File:** `src/App.jsx`

```jsx
import React from "react";

function Header() {
    return <header><h1>Student Portal</h1></header>;
}

function MainContent() {
    return <main><p>Welcome to the student portal.</p></main>;
}

function Footer() {
    return <footer><p>Copyright 2026 Student Portal</p></footer>;
}

function App() {
    return (
        <div>
            <Header />
            <MainContent />
            <Footer />
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 31. Create Welcome and Footer components with name and college

**File:** `src/Welcome.jsx`

```jsx
import React from "react";

function Welcome() {
    return (
        <section>
            <h1>Welcome, Harsh Gupta</h1>
            <p>Welcome to my student profile.</p>
        </section>
    );
}

export default Welcome;
```

**File:** `src/Footer.jsx`

```jsx
import React from "react";

function Footer() {
    return (
        <footer>
            <p>College: Your College Name</p>
        </footer>
    );
}

export default Footer;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import Welcome from "./Welcome.jsx";
import Footer from "./Footer.jsx";

function App() {
    return (
        <div>
            <Welcome />
            <Footer />
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 32. Apply CSS using an external CSS file

**File:** `src/App.jsx`

```jsx
import React from "react";
import "./App.css";

function App() {
    return (
        <div className="profile-card">
            <h1>Student Profile</h1>
            <p>Name: Harsh Gupta</p>
            <p>Course: BSc IT</p>
        </div>
    );
}

export default App;
```

**File:** `src/App.css`

```css
.profile-card {
    max-width: 420px;
    margin: 60px auto;
    padding: 24px;
    border: 2px solid #2563eb;
    border-radius: 12px;
    background-color: #eff6ff;
    font-family: Arial, sans-serif;
    text-align: center;
}

.profile-card h1 {
    color: #1d4ed8;
}

.profile-card p {
    color: #1f2937;
    font-size: 18px;
}
```

**Execution:** `npm run dev`

## 33. React component to add two numbers

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [firstNumber, setFirstNumber] = useState("");
    const [secondNumber, setSecondNumber] = useState("");
    const [sum, setSum] = useState(null);

    function calculateSum() {
        const first = Number(firstNumber);
        const second = Number(secondNumber);
        setSum(first + second);
    }

    return (
        <div>
            <h1>Add Two Numbers</h1>
            <label>
                First number:
                <input type="number" value={firstNumber} onChange={(event) => setFirstNumber(event.target.value)} />
            </label>
            <br />
            <label>
                Second number:
                <input type="number" value={secondNumber} onChange={(event) => setSecondNumber(event.target.value)} />
            </label>
            <br />
            <button onClick={calculateSum}>Calculate Sum</button>
            {sum !== null && <h2>Sum: {sum}</h2>}
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 34. Display date and time, updating every second

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";

function App() {
    const [currentDateTime, setCurrentDateTime] = useState(new Date());

    useEffect(() => {
        const timerId = setInterval(() => {
            setCurrentDateTime(new Date());
        }, 1000);

        return () => {
            clearInterval(timerId);
        };
    }, []);

    return (
        <div>
            <h1>Current Date and Time</h1>
            <p>{currentDateTime.toLocaleDateString()}</p>
            <p>{currentDateTime.toLocaleTimeString()}</p>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 35. Pass student details through props

**File:** `src/Student.jsx`

```jsx
import React from "react";

function Student(props) {
    return (
        <div>
            <h2>Student Details</h2>
            <p>Name: {props.name}</p>
            <p>Roll Number: {props.rollNumber}</p>
            <p>Course: {props.course}</p>
        </div>
    );
}

export default Student;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import Student from "./Student.jsx";

function App() {
    return (
        <div>
            <Student name="Harsh Gupta" rollNumber="IT24011" course="BSc IT" />
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 36. Product component accepting name and price through props

**File:** `src/Product.jsx`

```jsx
import React from "react";

function Product(props) {
    return (
        <article>
            <h2>{props.productName}</h2>
            <p>Price: ₹{props.price}</p>
        </article>
    );
}

export default Product;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import Product from "./Product.jsx";

function App() {
    return (
        <div>
            <h1>Product List</h1>
            <Product productName="Keyboard" price={799} />
            <Product productName="Mouse" price={499} />
            <Product productName="Headphones" price={1499} />
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 37. Use `useState` to manage and update data

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [message, setMessage] = useState("Initial message");

    function updateMessage() {
        setMessage("The message has been updated.");
    }

    return (
        <div>
            <h1>useState Example</h1>
            <p>{message}</p>
            <button onClick={updateMessage}>Update Message</button>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 38. Display and update a user's name using `useState`

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [name, setName] = useState("Harsh");

    function changeName() {
        setName("Harsh Gupta");
    }

    return (
        <div>
            <h1>User Name</h1>
            <p>Name: {name}</p>
            <button onClick={changeName}>Update Name</button>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 39. Counter with increment, decrement and reset

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [count, setCount] = useState(0);

    function increment() {
        setCount((previousCount) => previousCount + 1);
    }

    function decrement() {
        setCount((previousCount) => previousCount - 1);
    }

    function reset() {
        setCount(0);
    }

    return (
        <div>
            <h1>Counter: {count}</h1>
            <button onClick={increment}>Increment</button>
            <button onClick={decrement}>Decrement</button>
            <button onClick={reset}>Reset</button>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 40. Store a list in state and display it using `map()`

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [items, setItems] = useState(["Notebook", "Pen", "Pencil"]);
    const [newItem, setNewItem] = useState("");

    function addItem() {
        const trimmedItem = newItem.trim();

        if (trimmedItem !== "") {
            setItems((previousItems) => [...previousItems, trimmedItem]);
            setNewItem("");
        }
    }

    return (
        <div>
            <h1>Item List</h1>
            <input value={newItem} onChange={(event) => setNewItem(event.target.value)} placeholder="Enter item" />
            <button onClick={addItem}>Add Item</button>
            <ul>
                {items.map((item, index) => (
                    <li key={`${item}-${index}`}>{item}</li>
                ))}
            </ul>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 41. Display a list of names using `map()`

**File:** `src/App.jsx`

```jsx
import React from "react";

function App() {
    const names = ["Aarav", "Diya", "Kabir", "Meera", "Rohan"];

    return (
        <div>
            <h1>Names</h1>
            <ul>
                {names.map((name, index) => (
                    <li key={index}>{name}</li>
                ))}
            </ul>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 42. Display student details dynamically using JSX

**File:** `src/App.jsx`

```jsx
import React from "react";

function App() {
    const student = {
        name: "Harsh Gupta",
        rollNumber: "IT24011",
        course: "BSc IT",
        semester: 5,
        percentage: 82.5
    };

    return (
        <div>
            <h1>Student Details</h1>
            <p>Name: {student.name}</p>
            <p>Roll Number: {student.rollNumber}</p>
            <p>Course: {student.course}</p>
            <p>Semester: {student.semester}</p>
            <p>Percentage: {student.percentage}%</p>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 43. Calculate square and cube in React

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [number, setNumber] = useState("0");
    const numericNumber = Number(number);

    return (
        <div>
            <h1>Square and Cube Calculator</h1>
            <label>
                Enter a number:
                <input type="number" value={number} onChange={(event) => setNumber(event.target.value)} />
            </label>
            <p>Square: {numericNumber * numericNumber}</p>
            <p>Cube: {numericNumber * numericNumber * numericNumber}</p>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 44. To-do list with add and delete functionality

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [tasks, setTasks] = useState([]);
    const [taskText, setTaskText] = useState("");

    function addTask() {
        const trimmedTask = taskText.trim();

        if (trimmedTask === "") {
            return;
        }

        const newTask = {
            id: Date.now(),
            text: trimmedTask
        };

        setTasks((previousTasks) => [...previousTasks, newTask]);
        setTaskText("");
    }

    function deleteTask(taskId) {
        setTasks((previousTasks) => previousTasks.filter((task) => task.id !== taskId));
    }

    return (
        <div>
            <h1>To-do List</h1>
            <input value={taskText} onChange={(event) => setTaskText(event.target.value)} placeholder="Enter a task" />
            <button onClick={addTask}>Add Task</button>
            <ul>
                {tasks.map((task) => (
                    <li key={task.id}>
                        {task.text}
                        <button onClick={() => deleteTask(task.id)}>Delete</button>
                    </li>
                ))}
            </ul>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 45. Form that accepts user input and displays it dynamically

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [name, setName] = useState("");
    const [submittedName, setSubmittedName] = useState("");

    function handleSubmit(event) {
        event.preventDefault();
        setSubmittedName(name.trim());
    }

    return (
        <div>
            <h1>User Input Form</h1>
            <form onSubmit={handleSubmit}>
                <label>
                    Enter your name:
                    <input value={name} onChange={(event) => setName(event.target.value)} required />
                </label>
                <button type="submit">Submit</button>
            </form>
            {submittedName !== "" && <p>Your name is: {submittedName}</p>}
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 46. Registration form with name, email, phone and password validation

**File:** `src/App.jsx`

```jsx
import React, { useState } from "react";

function App() {
    const [formData, setFormData] = useState({
        name: "",
        email: "",
        phone: "",
        password: ""
    });
    const [errors, setErrors] = useState({});
    const [submitted, setSubmitted] = useState(false);

    function handleChange(event) {
        const { name, value } = event.target;
        setFormData((previousData) => ({
            ...previousData,
            [name]: value
        }));
    }

    function validateForm() {
        const newErrors = {};

        if (formData.name.trim().length < 2) {
            newErrors.name = "Name must contain at least 2 characters.";
        }

        if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(formData.email)) {
            newErrors.email = "Enter a valid email address.";
        }

        if (!/^[0-9]{10}$/.test(formData.phone)) {
            newErrors.phone = "Phone number must contain exactly 10 digits.";
        }

        if (formData.password.length < 8) {
            newErrors.password = "Password must contain at least 8 characters.";
        }

        return newErrors;
    }

    function handleSubmit(event) {
        event.preventDefault();
        const validationErrors = validateForm();
        setErrors(validationErrors);
        setSubmitted(Object.keys(validationErrors).length === 0);
    }

    return (
        <div>
            <h1>Registration Form</h1>
            <form onSubmit={handleSubmit} noValidate>
                <div>
                    <label htmlFor="name">Name:</label>
                    <input id="name" name="name" value={formData.name} onChange={handleChange} />
                    {errors.name && <p>{errors.name}</p>}
                </div>
                <div>
                    <label htmlFor="email">Email:</label>
                    <input id="email" name="email" type="email" value={formData.email} onChange={handleChange} />
                    {errors.email && <p>{errors.email}</p>}
                </div>
                <div>
                    <label htmlFor="phone">Phone Number:</label>
                    <input id="phone" name="phone" value={formData.phone} onChange={handleChange} />
                    {errors.phone && <p>{errors.phone}</p>}
                </div>
                <div>
                    <label htmlFor="password">Password:</label>
                    <input id="password" name="password" type="password" value={formData.password} onChange={handleChange} />
                    {errors.password && <p>{errors.password}</p>}
                </div>
                <button type="submit">Register</button>
            </form>
            {submitted && <p>Registration form validated successfully.</p>}
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 47. Display “Welcome to MERN Stack Development” using a Header component

**File:** `src/Header.jsx`

```jsx
import React from "react";

function Header() {
    return (
        <header>
            <h1>Welcome to MERN Stack Development</h1>
        </header>
    );
}

export default Header;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import Header from "./Header.jsx";

function App() {
    return (
        <div>
            <Header />
        </div>
    );
}

export default App;
```

**Execution:**
```bash
npm create vite@latest fsd-welcome-app -- --template react
cd fsd-welcome-app
npm install
npm run dev
```

---

# Q.1 — C. React Router and API Integration

## Setup for Questions 51–60

Inside the Vite React project, install the required packages:

```bash
npm install react-router-dom axios
```

## 51. Configure React Router and create Home, About and Contact pages

**File:** `src/main.jsx`

```jsx
import React from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
    <React.StrictMode>
        <BrowserRouter>
            <App />
        </BrowserRouter>
    </React.StrictMode>
);
```

**File:** `src/pages/Home.jsx`

```jsx
import React from "react";

function Home() {
    return <h1>Home Page</h1>;
}

export default Home;
```

**File:** `src/pages/About.jsx`

```jsx
import React from "react";

function About() {
    return <h1>About Page</h1>;
}

export default About;
```

**File:** `src/pages/Contact.jsx`

```jsx
import React from "react";

function Contact() {
    return <h1>Contact Page</h1>;
}

export default Contact;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home.jsx";
import About from "./pages/About.jsx";
import Contact from "./pages/Contact.jsx";

function App() {
    return (
        <div>
            <nav>
                <Link to="/">Home</Link>{" | "}
                <Link to="/about">About</Link>{" | "}
                <Link to="/contact">Contact</Link>
            </nav>
            <Routes>
                <Route path="/" element={<Home />} />
                <Route path="/about" element={<About />} />
                <Route path="/contact" element={<Contact />} />
            </Routes>
        </div>
    );
}

export default App;
```

**Execution:** `npm install react-router-dom` then `npm run dev`.

## 52. Use Link and Routes to navigate between pages

**File:** `src/App.jsx`

```jsx
import React from "react";
import { BrowserRouter, Routes, Route, Link } from "react-router-dom";

function Home() {
    return <h2>This is the Home page.</h2>;
}

function About() {
    return <h2>This is the About page.</h2>;
}

function Contact() {
    return <h2>This is the Contact page.</h2>;
}

function App() {
    return (
        <BrowserRouter>
            <div>
                <nav>
                    <Link to="/">Home</Link>{" | "}
                    <Link to="/about">About</Link>{" | "}
                    <Link to="/contact">Contact</Link>
                </nav>
                <Routes>
                    <Route path="/" element={<Home />} />
                    <Route path="/about" element={<About />} />
                    <Route path="/contact" element={<Contact />} />
                </Routes>
            </div>
        </BrowserRouter>
    );
}

export default App;
```

**Execution:** `npm install react-router-dom` then `npm run dev`.

## 53. Online bookstore with Home, Books, Cart and Page Not Found pages

**File:** `src/pages/Home.jsx`

```jsx
import React from "react";

function Home() {
    return (
        <section>
            <h1>Online Bookstore</h1>
            <p>Find your next favourite book.</p>
        </section>
    );
}

export default Home;
```

**File:** `src/pages/Books.jsx`

```jsx
import React from "react";

function Books() {
    const books = [
        { id: 1, title: "The Alchemist", price: 299 },
        { id: 2, title: "Wings of Fire", price: 250 },
        { id: 3, title: "Atomic Habits", price: 399 }
    ];

    return (
        <section>
            <h1>Books</h1>
            {books.map((book) => (
                <article key={book.id}>
                    <h2>{book.title}</h2>
                    <p>Price: ₹{book.price}</p>
                </article>
            ))}
        </section>
    );
}

export default Books;
```

**File:** `src/pages/Cart.jsx`

```jsx
import React from "react";

function Cart() {
    return (
        <section>
            <h1>Shopping Cart</h1>
            <p>Your cart is currently empty.</p>
        </section>
    );
}

export default Cart;
```

**File:** `src/pages/NotFound.jsx`

```jsx
import React from "react";

function NotFound() {
    return (
        <section>
            <h1>Page Not Found</h1>
            <p>The page you are looking for does not exist.</p>
        </section>
    );
}

export default NotFound;
```

**File:** `src/App.jsx`

```jsx
import React from "react";
import { BrowserRouter, Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home.jsx";
import Books from "./pages/Books.jsx";
import Cart from "./pages/Cart.jsx";
import NotFound from "./pages/NotFound.jsx";

function App() {
    return (
        <BrowserRouter>
            <div>
                <nav>
                    <Link to="/">Home</Link>{" | "}
                    <Link to="/books">Books</Link>{" | "}
                    <Link to="/cart">Cart</Link>
                </nav>
                <Routes>
                    <Route path="/" element={<Home />} />
                    <Route path="/books" element={<Books />} />
                    <Route path="/cart" element={<Cart />} />
                    <Route path="*" element={<NotFound />} />
                </Routes>
            </div>
        </BrowserRouter>
    );
}

export default App;
```

**Execution:** `npm install react-router-dom` then `npm run dev`.

## 54. Fetch public API data using Axios and display results

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [posts, setPosts] = useState([]);
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState("");

    useEffect(() => {
        axios.get("https://jsonplaceholder.typicode.com/posts")
            .then((response) => {
                setPosts(response.data);
                setLoading(false);
            })
            .catch(() => {
                setError("Unable to load posts.");
                setLoading(false);
            });
    }, []);

    if (loading) {
        return <p>Loading posts...</p>;
    }

    if (error) {
        return <p>{error}</p>;
    }

    return (
        <div>
            <h1>Posts from Public API</h1>
            {posts.slice(0, 10).map((post) => (
                <article key={post.id}>
                    <h2>{post.title}</h2>
                    <p>{post.body}</p>
                </article>
            ))}
        </div>
    );
}

export default App;
```

**Execution:** `npm install axios` then `npm run dev`.

## 55. Fetch users and filter by name using a search box

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [users, setUsers] = useState([]);
    const [searchText, setSearchText] = useState("");
    const [error, setError] = useState("");

    useEffect(() => {
        axios.get("https://jsonplaceholder.typicode.com/users")
            .then((response) => {
                setUsers(response.data);
            })
            .catch(() => {
                setError("Unable to fetch users.");
            });
    }, []);

    const filteredUsers = users.filter((user) => {
        return user.name.toLowerCase().includes(searchText.toLowerCase());
    });

    return (
        <div>
            <h1>Search Users</h1>
            <input
                type="text"
                value={searchText}
                onChange={(event) => setSearchText(event.target.value)}
                placeholder="Search by user name"
            />
            {error && <p>{error}</p>}
            <ul>
                {filteredUsers.map((user) => (
                    <li key={user.id}>
                        {user.name} — {user.email}
                    </li>
                ))}
            </ul>
        </div>
    );
}

export default App;
```

**Execution:** `npm install axios` then `npm run dev`.

## 56. Fetch sample data and dynamically display filtered results

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [products, setProducts] = useState([]);
    const [searchText, setSearchText] = useState("");
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState("");

    useEffect(() => {
        axios.get("https://dummyjson.com/products")
            .then((response) => {
                setProducts(response.data.products);
                setLoading(false);
            })
            .catch(() => {
                setError("Unable to fetch products.");
                setLoading(false);
            });
    }, []);

    const filteredProducts = products.filter((product) => {
        return product.title.toLowerCase().includes(searchText.toLowerCase());
    });

    if (loading) {
        return <p>Loading products...</p>;
    }

    return (
        <div>
            <h1>Product Search</h1>
            <input
                type="text"
                value={searchText}
                onChange={(event) => setSearchText(event.target.value)}
                placeholder="Search products"
            />
            {error && <p>{error}</p>}
            {filteredProducts.map((product) => (
                <article key={product.id}>
                    <h2>{product.title}</h2>
                    <p>Price: ₹{product.price}</p>
                </article>
            ))}
        </div>
    );
}

export default App;
```

**Execution:** `npm install axios` then `npm run dev`.

## 57. Fetch student data from an Express API using Axios

**File:** `backend/server.js`

```javascript
const express = require("express");
const cors = require("cors");

const app = express();
const PORT = 5000;

app.use(cors());
app.use(express.json());

const students = [
    { id: 1, name: "Aarav Sharma", rollNumber: "IT101", course: "BSc IT" },
    { id: 2, name: "Diya Patel", rollNumber: "IT102", course: "BSc IT" },
    { id: 3, name: "Kabir Singh", rollNumber: "IT103", course: "BSc IT" }
];

app.get("/api/students", (request, response) => {
    response.json(students);
});

app.listen(PORT, () => {
    console.log(`Student API running at http://localhost:${PORT}`);
});
```

**File:** `frontend/src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [students, setStudents] = useState([]);
    const [error, setError] = useState("");

    useEffect(() => {
        axios.get("http://localhost:5000/api/students")
            .then((response) => {
                setStudents(response.data);
            })
            .catch(() => {
                setError("Could not load student records.");
            });
    }, []);

    return (
        <div>
            <h1>Student Records</h1>
            {error && <p>{error}</p>}
            <table border="1" cellPadding="8">
                <thead>
                    <tr>
                        <th>ID</th>
                        <th>Name</th>
                        <th>Roll Number</th>
                        <th>Course</th>
                    </tr>
                </thead>
                <tbody>
                    {students.map((student) => (
                        <tr key={student.id}>
                            <td>{student.id}</td>
                            <td>{student.name}</td>
                            <td>{student.rollNumber}</td>
                            <td>{student.course}</td>
                        </tr>
                    ))}
                </tbody>
            </table>
        </div>
    );
}

export default App;
```

**Execution:**
```bash
# Terminal 1
mkdir backend
cd backend
npm init -y
npm install express cors
node server.js

# Terminal 2, from the folder containing backend/
npm create vite@latest frontend -- --template react
cd frontend
npm install
npm install axios
npm run dev
```

## 58. Display fetched data in a table

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";

function App() {
    const [comments, setComments] = useState([]);
    const [error, setError] = useState("");

    useEffect(() => {
        fetch("https://jsonplaceholder.typicode.com/comments?_limit=10")
            .then((response) => {
                if (!response.ok) {
                    throw new Error("Request failed");
                }
                return response.json();
            })
            .then((data) => {
                setComments(data);
            })
            .catch(() => {
                setError("Unable to load comments.");
            });
    }, []);

    return (
        <div>
            <h1>Comments</h1>
            {error && <p>{error}</p>}
            <table border="1" cellPadding="8">
                <thead>
                    <tr>
                        <th>ID</th>
                        <th>Name</th>
                        <th>Email</th>
                        <th>Comment</th>
                    </tr>
                </thead>
                <tbody>
                    {comments.map((comment) => (
                        <tr key={comment.id}>
                            <td>{comment.id}</td>
                            <td>{comment.name}</td>
                            <td>{comment.email}</td>
                            <td>{comment.body}</td>
                        </tr>
                    ))}
                </tbody>
            </table>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 59. Implement filter functionality on displayed data

**File:** `src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";

function App() {
    const [users, setUsers] = useState([]);
    const [searchText, setSearchText] = useState("");

    useEffect(() => {
        fetch("https://jsonplaceholder.typicode.com/users")
            .then((response) => response.json())
            .then((data) => setUsers(data))
            .catch((error) => console.error("Error fetching users:", error));
    }, []);

    const filteredUsers = users.filter((user) => {
        const search = searchText.toLowerCase();
        return user.name.toLowerCase().includes(search) ||
            user.email.toLowerCase().includes(search);
    });

    return (
        <div>
            <h1>Filter Users</h1>
            <input
                type="text"
                value={searchText}
                onChange={(event) => setSearchText(event.target.value)}
                placeholder="Search by name or email"
            />
            <ul>
                {filteredUsers.map((user) => (
                    <li key={user.id}>
                        <strong>{user.name}</strong> — {user.email}
                    </li>
                ))}
            </ul>
        </div>
    );
}

export default App;
```

**Execution:** `npm run dev`

## 60. Create a React form to send user data to the backend

**File:** `backend/server.js`

```javascript
const express = require("express");
const cors = require("cors");

const app = express();
const PORT = 5000;

app.use(cors());
app.use(express.json());

const users = [];
let nextId = 1;

app.post("/api/users", (request, response) => {
    const { name, email } = request.body;

    if (!name || !email) {
        return response.status(400).json({
            message: "Name and email are required."
        });
    }

    const newUser = {
        id: nextId++,
        name: name.trim(),
        email: email.trim()
    };

    users.push(newUser);

    response.status(201).json({
        message: "User created successfully.",
        user: newUser
    });
});

app.get("/api/users", (request, response) => {
    response.json(users);
});

app.listen(PORT, () => {
    console.log(`Backend server running at http://localhost:${PORT}`);
});
```

**File:** `frontend/src/App.jsx`

```jsx
import React, { useState } from "react";
import axios from "axios";

function App() {
    const [name, setName] = useState("");
    const [email, setEmail] = useState("");
    const [message, setMessage] = useState("");
    const [error, setError] = useState("");

    async function handleSubmit(event) {
        event.preventDefault();
        setMessage("");
        setError("");

        try {
            const response = await axios.post("http://localhost:5000/api/users", {
                name: name,
                email: email
            });

            setMessage(response.data.message);
            setName("");
            setEmail("");
        } catch (requestError) {
            setError(requestError.response?.data?.message || "Unable to submit user details.");
        }
    }

    return (
        <div>
            <h1>Send User Details</h1>
            <form onSubmit={handleSubmit}>
                <div>
                    <label htmlFor="name">Name:</label>
                    <input
                        id="name"
                        type="text"
                        value={name}
                        onChange={(event) => setName(event.target.value)}
                        required
                    />
                </div>
                <div>
                    <label htmlFor="email">Email:</label>
                    <input
                        id="email"
                        type="email"
                        value={email}
                        onChange={(event) => setEmail(event.target.value)}
                        required
                    />
                </div>
                <button type="submit">Submit</button>
            </form>
            {message && <p>{message}</p>}
            {error && <p>{error}</p>}
        </div>
    );
}

export default App;
```

**Execution:**
```bash
# Terminal 1
cd backend
npm init -y
npm install express cors
node server.js

# Terminal 2
cd frontend
npm install
npm install axios
npm run dev
```

---

# Q.2 — A. Node.js and Express

## Express setup

For the Node.js and Express questions, create a folder for the practical, open a terminal in that folder, and run:

```bash
npm init -y
npm install express
```

Create the specified file and run `node filename.js`. Each question below is a separate practical unless stated otherwise.

## 1. Display a message in the browser using a server response

**File:** `q2_01_browser_message.js`

```javascript
const http = require("http");

const server = http.createServer((request, response) => {
    response.writeHead(200, { "Content-Type": "text/html" });
    response.end("<h1>Hello from Node.js server</h1>");
});

const PORT = 3000;

server.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `node q2_01_browser_message.js`; open `http://localhost:3000`.

## 2. Create different routes in Express

**File:** `q2_02_routes.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.get("/", (request, response) => {
    response.send("Home Route");
});

app.get("/about", (request, response) => {
    response.send("About Route");
});

app.get("/contact", (request, response) => {
    response.send("Contact Route");
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_02_routes.js`; visit `/`, `/about` and `/contact`.

## 3. Send a JSON response from the server

**File:** `q2_03_json_response.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.get("/student", (request, response) => {
    response.json({
        name: "Harsh Gupta",
        rollNumber: "IT24011",
        course: "BSc IT"
    });
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_03_json_response.js`; open `http://localhost:3000/student`.

## 4. Create a simple REST API using Express

**File:** `q2_04_rest_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.use(express.json());

let products = [
    { id: 1, name: "Laptop", price: 45000 },
    { id: 2, name: "Mouse", price: 500 },
    { id: 3, name: "Keyboard", price: 1200 }
];

app.get("/api/products", (request, response) => {
    response.json(products);
});

app.get("/api/products/:id", (request, response) => {
    const product = products.find((item) => item.id === Number(request.params.id));

    if (!product) {
        return response.status(404).json({ message: "Product not found." });
    }

    response.json(product);
});

app.post("/api/products", (request, response) => {
    const { name, price } = request.body;

    if (!name || price === undefined) {
        return response.status(400).json({ message: "Name and price are required." });
    }

    const product = {
        id: products.length ? Math.max(...products.map((item) => item.id)) + 1 : 1,
        name: name,
        price: Number(price)
    };

    products.push(product);
    response.status(201).json(product);
});

app.listen(PORT, () => {
    console.log(`REST API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_04_rest_api.js`; test `http://localhost:3000/api/products`.

## 5. Implement a GET API to retrieve data

**File:** `q2_05_get_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

const students = [
    { id: 1, name: "Aarav", course: "BSc IT" },
    { id: 2, name: "Diya", course: "BSc IT" },
    { id: 3, name: "Kabir", course: "BSc IT" }
];

app.get("/api/students", (request, response) => {
    response.status(200).json(students);
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_05_get_api.js`; open `http://localhost:3000/api/students`.

## 6. Display “Welcome to Node.js and Express”

**File:** `q2_06_welcome_express.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.get("/", (request, response) => {
    response.send("Welcome to Node.js and Express");
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_06_welcome_express.js`.

## 7. Separate routes for Home, About, Services and Contact

**File:** `q2_07_multiple_routes.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.get("/", (request, response) => {
    response.send("<h1>Home Page</h1>");
});

app.get("/about", (request, response) => {
    response.send("<h1>About Page</h1>");
});

app.get("/services", (request, response) => {
    response.send("<h1>Services Page</h1>");
});

app.get("/contact", (request, response) => {
    response.send("<h1>Contact Page</h1>");
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_07_multiple_routes.js`.

## 8. Middleware that logs request method and URL

**File:** `q2_08_logger_middleware.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.use((request, response, next) => {
    console.log("Request Method:", request.method);
    console.log("Request URL:", request.url);
    console.log("Request Time:", new Date().toLocaleString());
    next();
});

app.get("/", (request, response) => {
    response.send("Request logged by middleware.");
});

app.get("/about", (request, response) => {
    response.send("About page");
});

app.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_08_logger_middleware.js`.

## 9. Library server with `/books` and `/members` routes

**File:** `q2_09_library_routes.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

const books = [
    { id: 1, title: "The Alchemist", author: "Paulo Coelho" },
    { id: 2, title: "Wings of Fire", author: "A. P. J. Abdul Kalam" }
];

const members = [
    { id: 1, name: "Aarav Sharma" },
    { id: 2, name: "Diya Patel" }
];

app.get("/books", (request, response) => {
    response.json(books);
});

app.get("/members", (request, response) => {
    response.json(members);
});

app.listen(PORT, () => {
    console.log(`Library server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_09_library_routes.js`.

## 10. Display products in JSON format

**File:** `q2_10_products_json.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

const products = [
    { id: 1, name: "Laptop", price: 45000 },
    { id: 2, name: "Mobile", price: 18000 },
    { id: 3, name: "Headphones", price: 1500 }
];

app.get("/products", (request, response) => {
    response.json(products);
});

app.listen(PORT, () => {
    console.log(`Product server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_10_products_json.js`; open `http://localhost:3000/products`.

## 11. GET `/api/books` and test in browser/Postman

**File:** `q2_11_books_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

const books = [
    { id: 1, title: "The Alchemist", author: "Paulo Coelho", available: true },
    { id: 2, title: "Wings of Fire", author: "A. P. J. Abdul Kalam", available: true },
    { id: 3, title: "Atomic Habits", author: "James Clear", available: false }
];

app.get("/api/books", (request, response) => {
    response.status(200).json(books);
});

app.listen(PORT, () => {
    console.log(`Books API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_11_books_api.js`; open `http://localhost:3000/api/books` or send a GET request to that URL in Postman.

## 12. REST API welcome message

**File:** `q2_12_welcome_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.get("/api/welcome", (request, response) => {
    response.status(200).json({
        message: "Welcome to the REST API"
    });
});

app.listen(PORT, () => {
    console.log(`API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_12_welcome_api.js`; open `http://localhost:3000/api/welcome`.

## 13. GET APIs for all students and a student by ID

**File:** `q2_13_students_get_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

const students = [
    { id: 1, name: "Aarav Sharma", rollNumber: "IT101", course: "BSc IT" },
    { id: 2, name: "Diya Patel", rollNumber: "IT102", course: "BSc IT" },
    { id: 3, name: "Kabir Singh", rollNumber: "IT103", course: "BSc IT" }
];

app.get("/api/students", (request, response) => {
    response.json(students);
});

app.get("/api/students/:id", (request, response) => {
    const student = students.find((item) => item.id === Number(request.params.id));

    if (!student) {
        return response.status(404).json({ message: "Student not found." });
    }

    response.json(student);
});

app.listen(PORT, () => {
    console.log(`Student API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_13_students_get_api.js`. Test `/api/students` and `/api/students/1`.

## 14. POST API to accept new student details

**File:** `q2_14_students_post_api.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.use(express.json());

const students = [
    { id: 1, name: "Aarav Sharma", rollNumber: "IT101", course: "BSc IT" }
];

app.get("/api/students", (request, response) => {
    response.json(students);
});

app.post("/api/students", (request, response) => {
    const { name, rollNumber, course } = request.body;

    if (!name || !rollNumber || !course) {
        return response.status(400).json({
            message: "Name, roll number and course are required."
        });
    }

    const newStudent = {
        id: students.length ? Math.max(...students.map((student) => student.id)) + 1 : 1,
        name: name,
        rollNumber: rollNumber,
        course: course
    };

    students.push(newStudent);

    response.status(201).json({
        message: "Student added successfully.",
        student: newStudent
    });
});

app.listen(PORT, () => {
    console.log(`Student API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_14_students_post_api.js`. In Postman use POST `http://localhost:3000/api/students`, select Body → raw → JSON, and send:
```json
{
    "name": "Meera Shah",
    "rollNumber": "IT104",
    "course": "BSc IT"
}
```

## 15. Implement frontend form validation with Node.js and Express

**File:** `q2_15_form_validation.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.use(express.urlencoded({ extended: true }));

app.get("/", (request, response) => {
    response.send(`
        <!DOCTYPE html>
        <html>
        <head>
            <title>Registration Form</title>
        </head>
        <body>
            <h1>Registration Form</h1>
            <form method="POST" action="/register">
                <label for="name">Name:</label>
                <input id="name" name="name" type="text" required minlength="2">
                <br><br>
                <label for="email">Email:</label>
                <input id="email" name="email" type="email" required>
                <br><br>
                <label for="phone">Phone:</label>
                <input id="phone" name="phone" type="tel" pattern="[0-9]{10}" required>
                <br><br>
                <label for="password">Password:</label>
                <input id="password" name="password" type="password" minlength="8" required>
                <br><br>
                <button type="submit">Register</button>
            </form>
        </body>
        </html>
    `);
});

app.post("/register", (request, response) => {
    const { name, email, phone, password } = request.body;
    const errors = [];

    if (!name || name.trim().length < 2) {
        errors.push("Name must contain at least 2 characters.");
    }

    if (!email || !/^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/.test(email)) {
        errors.push("Enter a valid email address.");
    }

    if (!phone || !/^[0-9]{10}$/.test(phone)) {
        errors.push("Phone number must contain exactly 10 digits.");
    }

    if (!password || password.length < 8) {
        errors.push("Password must contain at least 8 characters.");
    }

    if (errors.length > 0) {
        return response.status(400).send(`
            <h1>Validation Failed</h1>
            <ul>${errors.map((error) => `<li>${error}</li>`).join("")}</ul>
            <a href="/">Go back</a>
        `);
    }

    response.send(`<h1>Registration successful for ${name.trim()}</h1>`);
});

app.listen(PORT, () => {
    console.log(`Form server running at http://localhost:${PORT}`);
});
```

**Execution:** `npm install express` then `node q2_15_form_validation.js`; open `http://localhost:3000`.

## 16. Integrate a React frontend with Node.js and Express backend

**File:** `backend/server.js`

```javascript
const express = require("express");
const cors = require("cors");

const app = express();
const PORT = 5000;

app.use(cors());
app.use(express.json());

app.get("/api/message", (request, response) => {
    response.json({
        message: "React frontend connected to Express backend successfully."
    });
});

app.listen(PORT, () => {
    console.log(`Backend running at http://localhost:${PORT}`);
});
```

**File:** `frontend/src/App.jsx`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [message, setMessage] = useState("");
    const [error, setError] = useState("");

    useEffect(() => {
        axios.get("http://localhost:5000/api/message")
            .then((response) => {
                setMessage(response.data.message);
            })
            .catch(() => {
                setError("Could not connect to the Express backend.");
            });
    }, []);

    return (
        <div>
            <h1>React and Express Integration</h1>
            {message && <p>{message}</p>}
            {error && <p>{error}</p>}
        </div>
    );
}

export default App;
```

**Execution:**
```bash
# Terminal 1
cd backend
npm init -y
npm install express cors
node server.js

# Terminal 2
cd frontend
npm install
npm install axios
npm run dev
```

---

# Q.2 — B. MongoDB Database Operations

## MongoDB setup notes

- Install MongoDB Community Server and MongoDB Shell (`mongosh`), or use a MongoDB Atlas cluster.
- For shell questions, run the commands in `mongosh`.
- For Node.js questions using the MongoDB driver, install `npm install mongodb`.
- For Mongoose questions, install `npm install mongoose`.
- The Node.js examples below use `mongodb://127.0.0.1:27017` for a local MongoDB server. For Atlas, use your own connection string and keep credentials private.

## 17. Create a database and collection and insert records

**File:** `q2_17_database_collection.js` — run in `mongosh`

```javascript
use CollegeDB

db.createCollection("Students")

db.Students.insertMany([
    {
        rollNumber: "IT101",
        name: "Aarav Sharma",
        course: "BSc IT",
        marks: 82
    },
    {
        rollNumber: "IT102",
        name: "Diya Patel",
        course: "BSc IT",
        marks: 91
    },
    {
        rollNumber: "IT103",
        name: "Kabir Singh",
        course: "BSc IT",
        marks: 68
    }
])

db.Students.find()
```

**Execution:** Open `mongosh`, then run the commands above.

## 18. Connect MongoDB with Node.js

**File:** `q2_18_connect_mongodb.js`

```javascript
const { MongoClient } = require("mongodb");

const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

async function connectToMongoDB() {
    try {
        await client.connect();
        console.log("Connected to MongoDB successfully.");

        const database = client.db("CollegeDB");
        console.log("Database selected:", database.databaseName);
    } catch (error) {
        console.error("MongoDB connection error:", error);
    } finally {
        await client.close();
    }
}

connectToMongoDB();
```

**Execution:**
```bash
npm init -y
npm install mongodb
node q2_18_connect_mongodb.js
```

## 19. Store data in MongoDB

**File:** `q2_19_store_data.js`

```javascript
const { MongoClient } = require("mongodb");

const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

async function storeStudent() {
    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const students = database.collection("Students");

        const student = {
            rollNumber: "IT104",
            name: "Meera Shah",
            course: "BSc IT",
            marks: 86
        };

        const result = await students.insertOne(student);

        console.log("Student inserted successfully.");
        console.log("Inserted document ID:", result.insertedId);
    } catch (error) {
        console.error("Error storing student:", error);
    } finally {
        await client.close();
    }
}

storeStudent();
```

**Execution:** `npm install mongodb` then `node q2_19_store_data.js`.

## 20. Insert and update records in MongoDB

**File:** `q2_20_insert_update.js`

```javascript
const { MongoClient } = require("mongodb");

const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

async function insertAndUpdateStudent() {
    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const students = database.collection("Students");

        await students.insertOne({
            rollNumber: "IT105",
            name: "Rohan Verma",
            course: "BSc IT",
            marks: 72
        });

        console.log("Student inserted.");

        const updateResult = await students.updateOne(
            { rollNumber: "IT105" },
            { $set: { marks: 88, course: "BSc Information Technology" } }
        );

        console.log("Matched documents:", updateResult.matchedCount);
        console.log("Modified documents:", updateResult.modifiedCount);

        const updatedStudent = await students.findOne({ rollNumber: "IT105" });
        console.log("Updated student:", updatedStudent);
    } catch (error) {
        console.error("Insert/update error:", error);
    } finally {
        await client.close();
    }
}

insertAndUpdateStudent();
```

**Execution:** `npm install mongodb` then `node q2_20_insert_update.js`.

## 21. Insert and delete records in MongoDB

**File:** `q2_21_insert_delete.js`

```javascript
const { MongoClient } = require("mongodb");

const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

async function insertAndDeleteStudent() {
    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const students = database.collection("Students");

        const insertResult = await students.insertOne({
            rollNumber: "IT106",
            name: "Neha Joshi",
            course: "BSc IT",
            marks: 79
        });

        console.log("Inserted student ID:", insertResult.insertedId);

        const deleteResult = await students.deleteOne({ rollNumber: "IT106" });

        console.log("Deleted documents:", deleteResult.deletedCount);
    } catch (error) {
        console.error("Insert/delete error:", error);
    } finally {
        await client.close();
    }
}

insertAndDeleteStudent();
```

**Execution:** `npm install mongodb` then `node q2_21_insert_delete.js`.

## 22. Retrieve and display user data from MongoDB using Express

**File:** `q2_22_users_mongodb_express.js`

```javascript
const express = require("express");
const { MongoClient } = require("mongodb");

const app = express();
const PORT = 3000;
const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

app.get("/api/users", async (request, response) => {
    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const users = database.collection("Users");
        const allUsers = await users.find({}).toArray();

        response.json(allUsers);
    } catch (error) {
        console.error("Error retrieving users:", error);
        response.status(500).json({ message: "Unable to retrieve users." });
    }
});

app.listen(PORT, () => {
    console.log(`User API running at http://localhost:${PORT}`);
});
```

**Execution:**
```bash
npm init -y
npm install express mongodb
node q2_22_users_mongodb_express.js
```
Open `http://localhost:3000/api/users`. Insert some documents into `CollegeDB.Users` first.

## 23. API to add user details using Express and MongoDB

**File:** `q2_23_add_user_api.js`

```javascript
const express = require("express");
const { MongoClient } = require("mongodb");

const app = express();
const PORT = 3000;
const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

app.use(express.json());

app.post("/api/users", async (request, response) => {
    const { name, email, age } = request.body;

    if (!name || !email) {
        return response.status(400).json({
            message: "Name and email are required."
        });
    }

    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const users = database.collection("Users");

        const newUser = {
            name: name.trim(),
            email: email.trim(),
            age: age === undefined ? null : Number(age)
        };

        const result = await users.insertOne(newUser);

        response.status(201).json({
            message: "User added successfully.",
            insertedId: result.insertedId,
            user: newUser
        });
    } catch (error) {
        console.error("Error adding user:", error);
        response.status(500).json({ message: "Unable to add user." });
    }
});

app.get("/api/users", async (request, response) => {
    try {
        await client.connect();

        const database = client.db("CollegeDB");
        const users = database.collection("Users");
        const allUsers = await users.find({}).toArray();

        response.json(allUsers);
    } catch (error) {
        console.error("Error retrieving users:", error);
        response.status(500).json({ message: "Unable to retrieve users." });
    }
});

app.listen(PORT, () => {
    console.log(`User API running at http://localhost:${PORT}`);
});
```

**Execution:** `npm init -y`, `npm install express mongodb`, then `node q2_23_add_user_api.js`. Use Postman POST `http://localhost:3000/api/users` with JSON body:
```json
{
    "name": "Harsh Gupta",
    "email": "harsh@example.com",
    "age": 21
}
```

## 24. CollegeDB operations: insert, find by roll number, marks greater than 75, deleteOne

**File:** `q2_24_collegedb_operations.js` — run in `mongosh`

```javascript
use CollegeDB

db.Students.insertMany([
    { rollNumber: "IT201", name: "Aarav Sharma", marks: 82, course: "BSc IT" },
    { rollNumber: "IT202", name: "Diya Patel", marks: 91, course: "BSc IT" },
    { rollNumber: "IT203", name: "Kabir Singh", marks: 68, course: "BSc IT" },
    { rollNumber: "IT204", name: "Meera Shah", marks: 77, course: "BSc IT" }
])

db.Students.findOne({ rollNumber: "IT202" })

db.Students.find({ marks: { $gt: 75 } })

db.Students.deleteOne({ rollNumber: "IT203" })

db.Students.find()
```

**Execution:** Open `mongosh`, then run the commands above. If you have already inserted these roll numbers, use new roll numbers to avoid duplicate sample records.

## 25. Insert multiple student documents and display all records using `find()`

**File:** `q2_25_insert_many_students.js` — run in `mongosh`

```javascript
use CollegeDB

db.Students.insertMany([
    { rollNumber: "IT301", name: "Aarav Sharma", marks: 81, course: "BSc IT" },
    { rollNumber: "IT302", name: "Diya Patel", marks: 94, course: "BSc IT" },
    { rollNumber: "IT303", name: "Kabir Singh", marks: 73, course: "BSc IT" },
    { rollNumber: "IT304", name: "Meera Shah", marks: 88, course: "BSc IT" },
    { rollNumber: "IT305", name: "Rohan Verma", marks: 69, course: "BSc IT" }
])

db.Students.find()
```

**Execution:** Run the commands in `mongosh`.

## 26. Connect with Mongoose, insert a student and display it in the console

**File:** `q2_26_mongoose_student.js`

```javascript
const mongoose = require("mongoose");

const uri = "mongodb://127.0.0.1:27017/CollegeDB";

const studentSchema = new mongoose.Schema({
    rollNumber: {
        type: String,
        required: true
    },
    name: {
        type: String,
        required: true
    },
    course: {
        type: String,
        required: true
    },
    marks: {
        type: Number,
        required: true
    }
});

const Student = mongoose.model("Student", studentSchema);

async function insertStudent() {
    try {
        await mongoose.connect(uri);
        console.log("Connected to MongoDB using Mongoose.");

        const student = new Student({
            rollNumber: "IT401",
            name: "Aarav Sharma",
            course: "BSc IT",
            marks: 85
        });

        const savedStudent = await student.save();

        console.log("Student inserted successfully:");
        console.log(savedStudent);
    } catch (error) {
        console.error("Mongoose error:", error);
    } finally {
        await mongoose.disconnect();
    }
}

insertStudent();
```

**Execution:**
```bash
npm init -y
npm install mongoose
node q2_26_mongoose_student.js
```

## 27. Retrieve books from MongoDB using a GET API

**File:** `q2_27_books_get_mongodb.js`

```javascript
const express = require("express");
const { MongoClient } = require("mongodb");

const app = express();
const PORT = 3000;
const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

app.get("/api/books", async (request, response) => {
    try {
        await client.connect();

        const database = client.db("LibraryDB");
        const booksCollection = database.collection("Books");
        const books = await booksCollection.find({}).toArray();

        response.status(200).json(books);
    } catch (error) {
        console.error("Error retrieving books:", error);
        response.status(500).json({ message: "Unable to retrieve books." });
    }
});

app.listen(PORT, () => {
    console.log(`Books API running at http://localhost:${PORT}`);
});
```

**Execution:**
```bash
npm init -y
npm install express mongodb
node q2_27_books_get_mongodb.js
```

Insert sample records first in `mongosh`:
```javascript
use LibraryDB

db.Books.insertMany([
    { title: "The Alchemist", author: "Paulo Coelho", available: true },
    { title: "Wings of Fire", author: "A. P. J. Abdul Kalam", available: true },
    { title: "Atomic Habits", author: "James Clear", available: false }
])
```

Then open `http://localhost:3000/api/books` in the browser or send a GET request in Postman.

## 28. Use MongoDB comparison operators `$gt`, `$lt`, `$eq` and count records

**File:** `q2_28_comparison_operators.js` — run in `mongosh`

```javascript
use CollegeDB

db.Students.insertMany([
    { rollNumber: "IT501", name: "Aarav Sharma", marks: 82 },
    { rollNumber: "IT502", name: "Diya Patel", marks: 91 },
    { rollNumber: "IT503", name: "Kabir Singh", marks: 68 },
    { rollNumber: "IT504", name: "Meera Shah", marks: 75 },
    { rollNumber: "IT505", name: "Rohan Verma", marks: 88 }
])

db.Students.find({ marks: { $gt: 75 } })

db.Students.find({ marks: { $lt: 80 } })

db.Students.find({ marks: { $eq: 91 } })

db.Students.countDocuments({ marks: { $gt: 75 } })

db.Students.countDocuments({ marks: { $lt: 80 } })

db.Students.countDocuments({ marks: { $eq: 91 } })
```

**Execution:** Open `mongosh`, then run the commands above. Use new roll numbers if these sample records already exist.

---

## Important execution reminders

1. For a Node.js file, open the terminal in the directory where the file is saved and run `node filename.js`.
2. For React, run `npm run dev` from the Vite project folder and open the local URL shown in the terminal.
3. For Express, keep the server terminal running while testing the URL in a browser or Postman.
4. For frontend/backend practicals, start the backend and frontend in separate terminals.
5. For MongoDB examples, ensure the MongoDB service is running before executing the code.
6. The sample data is for practical demonstration. Some insertion examples may create duplicate sample records if run repeatedly; use fresh IDs or clear the test collection before repeating them.
