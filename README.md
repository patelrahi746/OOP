# Object Oriented Programming (CEUE203) — Lab Practical Repository

**Faculty of Engineering and Technology**  
**Academic Year:** 2026 – 2027 | **Semester:** 3  
**Course Code:** CEUE203  

This repository contains the complete practical work for the Object-Oriented Programming (Java) laboratory curriculum. The work is structured into two main parts:
- **Part A:** Core Practice Programs across 14 lab modules (located in `Practical-1` through `Practical-14`).
- **Part B:** **MiniBank** — An enterprise-style console banking application developed incrementally across the practicals (located in `Project/`).

---

## Repository Structure

```text
OOP/
├── Practical-1/          # Enums, Records, Switch Expressions (Vending Machine, Toll Booth, RPSLS)
├── Practical-2/          # Classes, Encapsulation, Constructor Chaining (Thermostat, Cinema, Parking)
├── Practical-3/          # Object Methods: equals, hashCode, toString (Points, Cards, Fractions)
├── Practical-4/          # Regex, Pattern Matching, StringBuilder (Password, Chat Filter, Templates)
├── Practical-5/          # Abstract Classes, Inheritance, Polymorphism (Shapes, Payroll, Media)
├── Practical-6/          # Interfaces, Lambdas, Functional Interfaces (Remote Control, Notifications)
├── Practical-7/          # Custom Annotations & Reflection (Form Validator, Test Runner, Column Mapper)
├── Practical-8/          # Exception Handling & AutoCloseable (Calculator, Warehouse, Resources)
├── Practical-9/          # Multithreading & Synchronization (Counter Race, Seat Booking, Array Sum)
├── Practical-10/         # Thread Pools, Producer-Consumer, Deadlocks (ExecutorService, Lock Ordering)
├── Practical-11/         # File I/O, Serialization & NIO (Save/Load, Log Analyzer, Tree Walker)
├── Practical-12/         # Java Collections Framework (Word Frequency, Unique Visitors, Leaderboard)
├── Practical-13/         # Generics, Bounded Types & Type Safety (Generic Containers, Stats, Generic Stack)
├── Practical-14/         # Layered Architecture, Packaging & Unit Testing (Layered App, Packaged App)
├── Project/              # Part B: MiniBank Banking Application (Complete Model, Service & CLI)
│   ├── minibank.jar      # Runnable application JAR
│   └── *.java            # Full source files for MiniBank
├── .gitignore
└── README.md
```

---

## Part A — Practical Breakdown

| Practical | Topics Covered | Key Programs |
|:---:|:---|:---|
| **[Practical-1](./Practical-1/)** | Enums, Switch expressions, Records, Scanner | `VendingMachine.java`, `TollBooth.java`, `RPSLS.java` |
| **[Practical-2](./Practical-2/)** | Encapsulation, Constructor chaining (`this()`), Static counters | `Thermostat.java`, `CinemaShow.java`, `ParkingLot.java` |
| **[Practical-3](./Practical-3/)** | Overriding `equals()`, `hashCode()`, `toString()` | `Point.java` + `Driver.java`, `Card.java` + `Driver2.java`, `Fraction.java` + `Driver3.java` |
| **[Practical-4](./Practical-4/)** | `String`, `StringBuilder`, `Pattern`, `Matcher`, `split()` | `PasswordChecker.java`, `ChatFilter.java`, `TemplateFiller.java` |
| **[Practical-5](./Practical-5/)** | Abstract classes, Dynamic dispatch, `super()`, `instanceof` | `Area.java` (Shapes), `Salary.java` (Payroll), `Main.java` (Media) |
| **[Practical-6](./Practical-6/)** | Interfaces, Default methods, Functional interfaces, Lambdas | `RemoteControl.java`, `Notifications.java`, `DiscountEngine.java` |
| **[Practical-7](./Practical-7/)** | Metadata annotations (`@Retention`, `@Target`), Reflection API | `FormValidator.java`, `MiniTestRunner.java`, `ColumnMapper.java` |
| **[Practical-8](./Practical-8/)** | Custom checked exceptions, `try-catch-finally`, `try-with-resources` | `GuardedCalculator.java`, `StockIssue.java`, `AutoCloseableDemo.java` |
| **[Practical-9](./Practical-9/)** | `Thread`, `Runnable`, Race conditions, `synchronized` blocks | `CounterRace.java`, `SeatBooking.java`, `ArraySum.java` |
| **[Practical-10](./Practical-10/)** | `ExecutorService`, `wait()`/`notify()`, Deadlock prevention | `ThreadPoolRunner.java`, `ProducerConsumer.java`, `DeadlockDemo.java` |
| **[Practical-11](./Practical-11/)** | Serialization (`Serializable`), `Path`, `Files`, NIO streams | `SaveLoad.java`, `LogAnalyzer.java`, `TreeWalker.java` |
| **[Practical-12](./Practical-12/)** | `List`, `Set`, `Map`, `Comparable`, `Comparator` | `WordFrequency.java`, `UniqueVisitors.java`, `Leaderboard.java` |
| **[Practical-13](./Practical-13/)** | Generic classes, Bounded type parameters (`<N extends Number>`) | `GenericContainers.java`, `BoundedStats.java`, `GenericStack.java` |
| **[Practical-14](./Practical-14/)** | Layered design, Packaging, Unit testing | `TinyLayeredApp.java`, `PackagedApp.java` |

---

## Part B — MiniBank Project

The `Project/` folder contains **MiniBank**, a full-featured console banking system built by applying all the OOP concepts learned across the semester:

- **Domain Model:** `Account` (abstract base), `SavingsAccount`, `CurrentAccount`, `FixedDepositAccount`, and `Customer` with nested `Address`.
- **Validation & Annotations:** Reflection-driven validation using `@Id`, `@Positive`, and `@MaxLength` annotations, combined with regex validation for mobile, email, PAN, and IFSC.
- **Robust Error Handling:** Custom checked exception hierarchy (`BankException`, `InsufficientFundsException`, `InvalidAmountException`, `AccountNotFoundException`).
- **Concurrent Processing:** Multi-threaded transaction engine using `ExecutorService`, thread-safe `ConcurrentHashMap`, and wait/notify synchronization.
- **Persistence & Audit Reporting:** Binary object serialization (`StatePersister`), append-only transaction logging (`TransactionLog`), and NIO directory reporting (`ReportGenerator`).
- **Generic Data Access:** Clean repository pattern (`Repository<T>`) using generics and reflection.
- **Interactive Console UI:** Menu-driven interface supporting account creation, deposits, withdrawals, transfers, account statements, and batch processing.

### Running MiniBank

To run the packaged executable JAR:
```bash
cd Project
java -jar minibank.jar
```

Or run directly from source:
```bash
cd Project
javac *.java
java MiniBankApp
```

---

## How to Compile & Run Practice Programs

You can compile and run any practical from the root directory or inside the respective folder using standard JDK commands:

```bash
# Example: Running Practical-1 TollBooth
javac Practical-1/TollBooth.java
java -cp Practical-1 TollBooth

# Example: Running Practical-9 Thread Safety Demo
javac Practical-9/counter-race/CounterRace.java
java -cp Practical-9/counter-race CounterRace
```
