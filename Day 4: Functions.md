Alright bro, chalona **Day 4: Functions** e deep dive kori 🚀.
Eita ekta crucial topic karon **React, Node.js, ba kono real-life industry project** — shobkichur backbone holo function.

---

# 📌 Day 4: Functions

## 🎯 Goal:

* Function er **syntax**, **type**, **parameters**, **return value** bujha
* **Real-life industry examples** diye practice kora
* **Lab session** kore ekdom hands-on feel neowa

---

## 1️⃣ Function Basics

### Syntax:

```js
function greetUser() {
  console.log("Hello, welcome to our system!");
}
greetUser();
```

👉 Ei type er function use hoy **Bkash app er welcome popup / first-time login greet message** er moto feature e.

---

## 2️⃣ Function with Parameters & Return

```js
function calculateBill(amount, vat) {
  let total = amount + (amount * vat / 100);
  return total;
}

console.log(calculateBill(1000, 15)); // 1150
```

👉 Ei logic ta use hoy **Restaurant POS system** e jekhane VAT add kora hoy.
**Bangladesh example**: Pizza Hut er POS machine exactly ei type math kore.

---

## 3️⃣ Function Expression

```js
const square = function (num) {
  return num * num;
};
console.log(square(5)); // 25
```

👉 Industry te frequently use hoy jodi **dynamic function pass** korte hoy.
Example: **Daraz e product filter function** (price, rating, discount).

---

## 4️⃣ Arrow Function (ES6)

```js
const discountPrice = (price, discount) => price - (price * discount / 100);

console.log(discountPrice(500, 10)); // 450
```

👉 Ei shortcut **React component** banate frequently use hoy.
Example:

```js
const Button = () => <button>Click Me</button>;
```

---

## 5️⃣ Default Parameters

```js
function sendSMS(message, sender = "System") {
  return `${sender}: ${message}`;
}
console.log(sendSMS("Your OTP is 1234"));  
```

👉 Real-life: **Bkash OTP SMS** er jonno default sender thake “bKash”.

---

## 6️⃣ Rest & Spread in Functions

```js
function sumAll(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sumAll(10, 20, 30, 40)); // 100
```

👉 **Bkash bulk payment API** ekbar e multiple transaction handle korte pare. Ei concept sekhane use hoy.

---

## 7️⃣ Higher Order Functions (HOF)

👉 Function jodi **another function return kore** or **parameter hisebe function ney**, take HOF bole.

```js
function operation(fn, x, y) {
  return fn(x, y);
}

const add = (a, b) => a + b;
const multiply = (a, b) => a * b;

console.log(operation(add, 5, 3));       // 8
console.log(operation(multiply, 5, 3)); // 15
```

👉 Industry example:
**Pathao ride-sharing system** – different pricing strategy (base fare, peak fare, discount fare). HOF diye implement kora easy.

---

# 🧪 Lab Sessions

### ✅ Lab 1: Currency Converter

* Input: Amount in BDT
* Output: Converted USD

```js
function convertBDTtoUSD(bdt, rate = 120) {
  return (bdt / rate).toFixed(2);
}
console.log(convertBDTtoUSD(1200)); // 10
```

### ✅ Lab 2: E-commerce Discount Calculator

* Input: Price, discount %
* Output: Final price

```js
function getDiscountedPrice(price, discount) {
  return price - (price * discount / 100);
}
console.log(getDiscountedPrice(2000, 20)); // 1600
```

### ✅ Lab 3: SMS Notification System

```js
function sendNotification(user, message) {
  return `${user}, you have a new notification: ${message}`;
}

console.log(sendNotification("Aliul", "Your delivery is on the way"));
```

---

# 🏢 Real-World Industry Usage

* **Bkash / Nagad**: Transaction validation er function (input amount → fees + vat → output total).
* **Daraz / AjkerDeal**: Discount, coupon, product filter calculation.
* **Pathao / Uber**: Fare calculation function (distance, base fare, discount).
* **Grameenphone IT**: Utility function (convert MB ↔ GB ↔ minutes).

---

👉 Bro, ekhane function er **basic to industry-level use-case** diye dilam.
Tumi chao naki ami **ekta mini-project (Function-based Calculator or Fare System)** build kore dite ei topic complete korte?
