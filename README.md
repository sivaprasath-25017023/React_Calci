# Ex04 Simple Calculator - React Project
## Date: 19-03-2026

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.
-
### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
### Calculatr.jsx

```
import React, { useState } from 'react';
import Display from './Display';
import Button from './Button';
import '../Calculator.css';

const Calculator = () => {
  const [input, setInput] = useState('');
  const [result, setResult] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setResult(eval(input).toString());
      } catch (error) {
        setResult('Error');
      }
    } else if (value === 'C') {
      setInput('');
      setResult('');
    } else {
      setInput(input + value);
    }
  };

  return (
    <div className="calculator">
      <Display input={input} result={result} />
      <div className="buttons">
        <Button onClick={handleClick} value="7" />
        <Button onClick={handleClick} value="8" />
        <Button onClick={handleClick} value="9" />
        <Button onClick={handleClick} value="/" />
        <Button onClick={handleClick} value="4" />
        <Button onClick={handleClick} value="5" />
        <Button onClick={handleClick} value="6" />
        <Button onClick={handleClick} value="*" />
        <Button onClick={handleClick} value="1" />
        <Button onClick={handleClick} value="2" />
        <Button onClick={handleClick} value="3" />
        <Button onClick={handleClick} value="-" />
        <Button onClick={handleClick} value="0" />
        <Button onClick={handleClick} value="." />
        <Button onClick={handleClick} value="=" />
        <Button onClick={handleClick} value="+" />
        <Button onClick={handleClick} value="C" />
      </div>
    </div>
  );
};

export default Calculator;

```

### Calculator.css
```
.calculator {
  width: 300px;
  margin: 50px auto;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.display {
  background-color: #f0f0f0;
  padding: 10px;
  text-align: right;
  border-bottom: 1px solid #ccc;
}

.input {
  font-size: 18px;
  min-height: 24px;
}

.result {
  font-size: 24px;
  font-weight: bold;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

button {
  width: 100%;
  padding: 15px;
  font-size: 18px;
  border: 1px solid #ccc;
  cursor: pointer;
  background-color: #fff;
}

button:hover {
  background-color: #f0f0f0;
}

```

### App.js
```
import React from 'react';
import Calculator from './components/Calculator';
import './App.css';

function App() {
  return (
    <div className="App">
      <Calculator />
    </div>
  );
}

export default App;
```
## OUTPUT
<img width="1919" height="1138" alt="Screenshot 2026-03-19 111911" src="https://github.com/user-attachments/assets/b35e0cfd-5913-46f2-825c-6dff2f0f501e" />
<img width="1919" height="1132" alt="Screenshot 2026-03-19 111954" src="https://github.com/user-attachments/assets/5e5789da-d0f5-4217-8782-c5a87072ea66" />




## RESULT
The program for developing a simple calculator in React.js is executed successfully.
