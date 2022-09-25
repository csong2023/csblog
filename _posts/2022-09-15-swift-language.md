---
layout: post
title: "Using polymorphic properties in OOP"
date: 2022-09-17 4:48:49 +0900
categories: Study
---

## Introduction

Polymorphism is one of the core concepts of object-oriented programming (OOP) and describes situations in which something occurs in several different forms. In computer science, it describes the concept that you can access objects of different types through the same interface. Each type can provide its own independent implementation of this interface. In today's experience with OOP, I was able to create multiple codes in different forms, while providing the same performance.

---

## Class (Inherited from Calculator)

```swift
class BetterCalculator {
    //ModelName, SerialNumber
    let modelName: String
    let serialNumber: String

    init(modelName: String, serialNumber: String) {
        self.modelName = modelName
        self.serialNumber = serialNumber
    }
    
    //Constructor == Initializer
    //Add, Subtract, Multiply
    func multiply(a: Int, b: Int) -> Int {
        return a * b
    }
    func add(a: Int, b: Int) -> Int {
        return a + b
    }
    func subtract(a: Int, b: Int) -> Int {
        return a - b
    }
    func power(a: Int) -> Int {
        return a * a
    }
}
```

Using a basic form of class, I was able to create a calculator that allows minimum computational functions.

## Alternate Form

```swift
class BetterCalculator {
    func power(a: Int) -> Int {
        return a * a
    }
}

let myBetterCalculator = BatterCalculator(modelName: "abc", serialnumber: "abc")
```

Then, a different form of the same function was created using the polymorphic qualities of swift.

---

## Conclusion

i was able to create multiple forms of the 'Calculator' function which is a collection of functions allowing basic computations.