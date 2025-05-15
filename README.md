
# 🏨 Hotel Management System

This is a simple Java-based application that simulates the core functionalities of a hotel management system. It supports room booking, food ordering, billing, and checkout operations. It also supports persistence using object serialization.

---

## 📋 Features

* Room booking:

  * Luxury Double Room
  * Deluxe Double Room
  * Luxury Single Room
  * Deluxe Single Room
* Food ordering with a predefined menu
* Room availability checking
* Bill generation (room + food)
* Room deallocation (checkout)
* Data persistence using object serialization (saved to `backup` file)

---

## 🧾 Food Menu

| Item No | Item     | Price (INR) |
| ------- | -------- | ----------- |
| 1       | Sandwich | 50          |
| 2       | Pasta    | 60          |
| 3       | Noodles  | 70          |
| 4       | Coke     | 30          |

---

## 🛏 Room Types & Charges

| Room Type          | Beds     | AC  | Breakfast | Price/Day (INR) |
| ------------------ | -------- | --- | --------- | --------------- |
| Luxury Double Room | 1 Double | Yes | Yes       | 4000            |
| Deluxe Double Room | 1 Double | No  | Yes       | 3000            |
| Luxury Single Room | 1 Single | Yes | Yes       | 2200            |
| Deluxe Single Room | 1 Single | No  | Yes       | 1200            |

---

## 🛠 How It Works

1. **Startup**:

   * If a backup file exists, the hotel state is restored.
2. **Main Menu Options**:

   * Display room details
   * Check room availability
   * Book a room
   * Order food for a room
   * Checkout and generate bill
   * Exit the system
3. **Data Persistence**:

   * On exit, the hotel state is saved in `backup` file using object serialization.

---

## 🚀 How to Run

### Requirements

* Java Development Kit (JDK) 8 or higher

### Compile

```bash
javac Main.java
```

### Run

```bash
java Main
```

---

## 🧠 Classes Overview

* **Main**: Entry point of the application. Manages the menu.
* **Hotel**: Contains all business logic.
* **holder**: Maintains all room objects.
* **Singleroom / Doubleroom**: Represents single and double rooms respectively.
* **Food**: Represents a food order.
* **NotAvailable**: Custom exception for unavailable rooms.
* **write**: Thread to persist hotel data.

---

## 💾 Persistence

* The system stores data in a file named `backup`.
* Upon restart, data is restored, enabling continuity between sessions.



