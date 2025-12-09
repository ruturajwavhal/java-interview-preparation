# java-interview-preparation


✅ What is String?

A String is an immutable sequence of characters.
Once created, it cannot be changed.

Example:
String s = "Hello";
s.concat("World");
System.out.println(s);   // Output: Hello (NOT HelloWorld)

Reason → String is immutable.

✅ What is StringBuffer?

StringBuffer is a mutable, thread-safe (synchronized) class used when we need to modify strings, especially in multi-threaded environments.

Example:
StringBuffer sb = new StringBuffer("Hello");
sb.append("World");
System.out.println(sb);  // Output: HelloWorld

✅ What is StringBuilder?

StringBuilder is also mutable, but NOT thread-safe (not synchronized).
It is faster than StringBuffer and used in single-threaded scenarios.

Example:
StringBuilder sb = new StringBuilder("Hello");
sb.append("World");
System.out.println(sb);  // Output: HelloWorld

🔥 Difference Between String, StringBuffer, StringBuilder

| Feature       | String                 | StringBuffer                    | StringBuilder                 |
| ------------- | ---------------------- | ------------------------------- | ----------------------------- |
| Mutability    | ❌ Immutable            | ✔ Mutable                       | ✔ Mutable                     |
| Thread Safety | Not thread-safe        | ✔ Thread-safe (synchronized)    | ❌ Not thread-safe             |
| Performance   | Slow for modifications | Slower (due to synchronization) | Fastest                       |
| When to Use   | Fixed text             | Multi-threaded modifications    | Single-threaded modifications |

Note - 
Specifically, "two or more threads cannot call the methods of StringBuffer simultaneously" implies that only one thread can execute a synchronized method of a StringBuffer instance at any given time. When one thread enters a synchronized method (like append(), insert(), delete(), etc.) of a StringBuffer object, a lock is acquired on that object. Any other thread attempting to call a synchronized method on the same StringBuffer object will be blocked and forced to wait until the first thread releases the lock.

⭐ Super-short interview answer (20 seconds)

String is immutable. StringBuffer and StringBuilder are mutable.
StringBuffer is thread-safe but slower. StringBuilder is not thread-safe but faster.
