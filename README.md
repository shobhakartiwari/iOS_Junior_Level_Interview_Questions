
# iOS Junior Level Interview Questions

> iOS Interview Questions - Your Cheat Sheet For iOS Interview

### Prepared & maintained by [Shobhakar Tiwari](https://github.com/shobhakartiwari) - Senior iOS Lead Engineer • Building for Apple Platforms!

## About me:  [DM for iOS Mock interview](https://www.linkedin.com/in/shobhakar-tiwari/)

Hi, I am Shobhakar Tiwari • I have taught and mentored many developers, and their efforts landed them high-paying tech jobs in United States, helped many tech companies in solving their unique problems, and created many framework for airline, e-Commerce based companies. I am passionate coding and always try to contribute to the developer community.

You can check my contributions over:

- [StackOverflow](https://stackoverflow.com/users/3400991/shobhakar-tiwari?tab=profile)
- [LinkedIn](https://www.linkedin.com/in/shobhakar-tiwari/)
- [GitHub](https://github.com/shobhakartiwari)

- 🔗 Feel free to explore my repositories to get a taste of my work, and don't hesitate to get in touch if you have any questions or collaboration ideas. Happy coding! 🎉

## Contents - iOS Interview Questions

# Swift Interview Questions

Welcome to the Swift Interview Questions repository! This document contains a curated list of essential interview questions that can help you prepare for iOS developer roles focusing on Swift programming. Each question is designed to test your knowledge of the Swift language, its features, and best practices.

## Questions

### 1. What is Swift language? Is it an OOP language or POP (Protocol Oriented Programming)?
*Answer:* Swift is a multi-paradigm programming language that supports both Object-Oriented Programming (OOP) and Protocol-Oriented Programming (POP). 

### 2. Why is Swift called Protocol Oriented Programming?
*Answer:* Swift emphasizes the use of protocols to define blueprints of methods, properties, and other requirements, promoting a flexible and modular design.

### 3. Why is Swift called a strictly type-safe language?
*Answer:* Swift enforces strong type-checking at compile time, reducing runtime crashes and errors by ensuring that variables are used with the correct data types.

### 4. What is Optional?
*Answer:* An Optional in Swift is a type that can hold either a value or `nil`, indicating the absence of a value.

### 5. Is Optional an ENUM or STRUCT?
*Answer:* Optional is an enumeration (ENUM) that has two cases: `.none` (for `nil`) and `.some(Wrapped)`.

### 6. What are the different ways of getting data from optionals?
*Answer:* You can retrieve data from optionals using optional binding (`if let`, `guard let`), forced unwrapping (`!`), or optional chaining.

### 7. What are the differences between `guard let` vs `if let`? When would you use `guard let` over `if let`?
*Answer:* `guard let` is used for early exits from a function or loop if the condition is not met, while `if let` allows you to handle the case where an optional contains a value. Use `guard let` for cleaner and more readable code when you need to exit early.

### 8. What is the force unwrapping operator and why is it not recommended?
*Answer:* The force unwrapping operator (`!`) is used to retrieve the value of an optional. It is not recommended because if the optional is `nil`, it will cause a runtime crash.

### 9. What is a mutable structure?
*Answer:* A mutable structure in Swift is a structure whose properties can be modified after its initial creation.

### 10. What is the `mutating` keyword and why is it needed?
*Answer:* The `mutating` keyword is used in methods of structures to indicate that the method can modify the properties of the structure itself.

### 11. What is a closure? Is a closure also a function?
*Answer:* A closure is a self-contained block of functionality that can be passed around and used in your code. Yes, closures can be thought of as anonymous functions.

### 12. Is closure a reference type or value type?
*Answer:* A closure is a reference type, which means it captures variables and constants from its surrounding context.

### 13. Create a function for finding the sum of two numbers and convert this into a sum closure.
```swift
func sum(a: Int, b: Int) -> Int {
    return a + b
}

let sumClosure: (Int, Int) -> Int = { a, b in
    return a + b
}
```

### 14. Create a structure of an Employee and within this, there should be one Department where the Department has an id and name.
*Answer:* 
```swift
struct Department {
    var id: Int
    var name: String
}

struct Employee {
    var id: Int
    var name: String
    var department: Department
}
```

### 15. What are access modifiers?
*Answer:* Access modifiers define the visibility of properties and methods in Swift, including public, private, fileprivate, and internal.

### 16. What is the difference between SceneDelegate and AppDelegate?
*Answer:* AppDelegate manages app-wide behavior, while SceneDelegate manages individual instances of UI. SceneDelegate allows multiple UI scenes to run simultaneously.

### 17. What is the use of SceneDelegate?
*Answer:* SceneDelegate is used to manage the lifecycle of a single scene in your app, including its creation and destruction.

### 18. What is a Tuple and where should you use it?
*Answer:* A tuple is a group of multiple values that can be of different types. They are useful for returning multiple values from a function.

### 19. What are higher-order functions?
*Answer:* Higher-order functions are functions that take other functions as parameters or return functions as their result.

### 20. Create an array of strings ["1", "3", "4", "6"] and find the sum of all even numbers using higher-order functions. Don’t use any loops!
*Answer:* 
```swift
let numbers = ["1", "3", "4", "6"]
let evenSum = numbers.compactMap { Int($0) }.filter { $0 % 2 == 0 }.reduce(0, +)
```
### 21. Create an array of Employees and try to filter out those who joined before Jan 2024.
*Answer:* 
```swift
struct Employee {
    var name: String
    var joiningDate: Date
}

let employees: [Employee] = [] // Assume this array is populated
let filteredEmployees = employees.filter { $0.joiningDate < Calendar.current.date(from: DateComponents(year: 2024, month: 1, day: 1))! }
```
### 22. What is Responder and what is its use?
*Answer:*  The Responder chain is a hierarchy of objects that can respond to events and handle user interactions in iOS.

### 23. What are the different options you have to store data locally?
*Answer:*  Options for local data storage include UserDefaults, Keychain, Core Data, and file storage.

### 24. What is the latest version of Xcode, Swift, iOS, and macOS?
*Answer:*  (Provide the current versions at the time of the interview)

### 25. Do you know about WWDC?
*Answer:* : Yes, WWDC (Worldwide Developers Conference) is an annual event held by Apple to showcase new software and technologies for developers.

### 26. What is iOS and how is it different from other mobile OS?
*Answer:*  iOS is Apple's mobile operating system, known for its user-friendly interface, security, and extensive ecosystem. It differs from Android and other OSes in its closed ecosystem and proprietary nature.

### 27. If your application is crashing, what are the different ways you can investigate to find out the issue?
*Answer:*  Use Xcode debugger, check crash logs, utilize instruments to track memory usage, and analyze code for potential issues.

### 28. What is Jailbreak and what is its impact?
*Answer:*  Jailbreaking is the process of removing software restrictions on iOS devices, allowing users to install unauthorized apps. It can compromise security and void warranties.

### 29. What frameworks are available to create UI in iOS?
*Answer:*  Common frameworks include UIKit, SwiftUI, and Interface Builder.

### 30. What is the difference between UIKit and SwiftUI?
*Answer:*  UIKit is the traditional framework for building iOS apps, while SwiftUI is a newer, declarative framework that allows for faster development and less boilerplate code.

### 31. What is an extension?
*Answer:*  An extension allows you to add functionality to existing classes, structures, or enumerations without modifying their original implementation.

### 32. Use this link: https://hp-api.onrender.com/ to get the data from the server and parse it in a playground to print it.
*Answer:* 
```swift
import Foundation

let url = URL(string: "https://hp-api.onrender.com/")!
let task = URLSession.shared.dataTask(with: url) { data, response, error in
    guard let data = data, error == nil else { return }
    // Parse data
}
task.resume()
```

### 33. What is Keychain? How will you decide whether to save data into Keychain or UserDefaults?
*Answer:* Keychain is a secure storage solution for sensitive data, while UserDefaults is used for storing user preferences. Use Keychain for sensitive information like passwords, and UserDefaults for simple user settings.

### 34. What is the problem with global variables?
*Answer:* Global variables can lead to namespace pollution, make code harder to test, and introduce unexpected side effects due to shared state.

### 35. What is Property Observer? Write an example.
*Answer:* Property observers allow you to respond to changes in a property’s value. Example:
```swift 
var observedProperty: Int = 0 {
    willSet {
        print("About to set: \(newValue)")
    }
    didSet {
        print("Just set: \(oldValue) to \(observedProperty)")
    }
}
```

### 36. What is Property Wrapper? Write code to showcase it.
*Answer:*  A property wrapper is a custom type that encapsulates the storage and behavior of a property. Example:
```swift
@propertyWrapper
struct Clamped<Value: Comparable> {
    private var value: Value
    private let range: ClosedRange<Value>
    
    var wrappedValue: Value {
        get { value }
        set { value = min(max(newValue, range.lowerBound), range.upperBound) }
    }
    
    init(wrappedValue: Value, _ range: ClosedRange<Value>) {
        self
```
### 37. Question: What sorting algorithm does the sorted() function in Swift use, and what is its time complexity in the average and worst-case scenarios?
*Answer:*
The sorted() function in Swift uses the Timsort algorithm, which is a hybrid sorting algorithm derived from merge sort and insertion sort. Its time complexity is as follows:

Average Case: O(n log n)
Worst Case: O(n log n)
Timsort is designed to perform well on many kinds of real-world data and is particularly efficient for data that is already partially sorted.
