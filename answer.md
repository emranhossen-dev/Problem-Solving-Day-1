# Day 1 — Theory Questions & Answers

### Q1. What is the difference between var, let, and const in JavaScript?
- **var:** Function-scoped, can be re-declared and updated, hoisted with `undefined`.
- **let:** Block-scoped, cannot be re-declared in the same scope, can be updated, lives in TDZ before declaration.
- **const:** Block-scoped, cannot be re-declared or reassigned, lives in TDZ before declaration.

---

### Q2. Explain the concept of hoisting in JavaScript.
JavaScript moves declarations to the top of their scope during compilation. Function declarations are hoisted completely, `var` is hoisted as `undefined`, and `let`/`const` are hoisted uninitialized.

---

### Q3. What are the primitive data types in JavaScript?
There are 7 primitive types: `string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, and `null`.

---

### Q4. What is the difference between == and === in JavaScript?
- `==` (Loose equality): Compares values after type conversion.
- `===` (Strict equality): Compares both value and data type without conversion.

---

### Q5. Explain how closures work in JavaScript with an example.
A closure allows an inner function to access variables from its outer function's scope even after the outer function has finished executing.

```javascript
function counter() {
  let count = 0;
  return () => ++count;
}
const countUp = counter();
countUp(); // 1
