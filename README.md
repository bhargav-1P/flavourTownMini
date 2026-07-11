#  FlavorTown Street Food - Day 17 Build

Welcome to the **FlavorTown Street Food** interactive menu application! This project represents a complete, ground-up rebuild designed to establish flawless frontend fundamentals. Built entirely from scratch, it serves as a core educational milestone in understanding semantic HTML structures, clean CSS card components, and interactive DOM manipulation using vanilla JavaScript.

---

## The Feature Engine: How It Works

Instead of overcomplicating the system with heavy external frameworks, this architecture utilizes a direct **Event-Driven UI Bridge**. Every interaction follows a strict three-step execution pipeline:

1. **The Event Trigger:** The user clicks an action button on a specific menu item. The `onclick` listener fires immediately, passing the raw numeric decimal price as a direct argument into our engine logic (`addToBill(8.99)`).
2. **The Memory Update:** Inside our JavaScript script execution context, an internal tracking state variable (`currentTotalMoney`) catches the parameter stream and updates its numeric balance using cumulative addition.
3. **The Live UI Render:** The script queries the browser DOM using the highly optimized `.getElementById("bill-total")` look-up tool. It completely overwrites the static text container content with the new calculated financial statement, using `.toFixed(2)` to ensure absolute currency accuracy on the screen.



---

## Code Architecture Blueprint

### 1. Structural Layer (`index.html`)
The application layout uses strict semantic tags (`<header>`, `<main>`, `<section>`) to define logical component domains. This ensures accessibility and a professional layout tree.

### 2. Styling Layer (Embedded CSS)
Every element is styled natively to avoid dependency bloat. Interactive components utilize:
* Clean canvas color contrasts (`#fcf8f2` body canvas against clean white card structures).
* Box-shadow dimensions for high-end component depth elevation (`0 2px 4px rgba(0,0,0,0.05)`).
* Responsive typography and micro-spaced button padding scales.

### 3. Logic Layer (Vanilla JavaScript)
```javascript
// 1. Core global memory boundary to preserve runtime state
let currentTotalMoney = 0;

// 2. Linear transaction processor execution boundary
function addToBill(itemPrice) {
    // Accumulate incoming floating-point data streams
    currentTotalMoney = currentTotalMoney + itemPrice;
    
    // Direct DOM write operation bypassing layout bottlenecks
    document.getElementById("bill-total").textContent = currentTotalMoney.toFixed(2);
}
