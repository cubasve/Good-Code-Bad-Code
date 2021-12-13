Good Code, Bad Code - Think like a software engineer (BY Tom Long)

# i. IN THEORY

## 1. Code Quality

- High-quality code maximizes the chance that the software will be reliable, maintainable, and meet its requirements. Low-quality code tends to do the opposite
  ![image](https://user-images.githubusercontent.com/62129720/144141518-a56968ff-e8e5-4cd5-b091-c594bc394a62.png)

**4 high-level goals to achieve when writing code**
| Goals | |
| ----------- | ----------- |
| It should work | |
| It should keep working | Code depends on other code that will get modified, updated, and changed. |
| It should be adaptable to changing requirements | Business realities shift, Consumer preferences change, Assumptions get invalidated, New features are continually added |
| It doesn't reinvent the wheel | Why use an existing solution rather than reinvent it? 1. It saves time and effort 2. It decreases the chance of bugs 3. It utilizes existing expertise 4. It makes code easier to understand |

**6 Pillars of Code Quality**
| Make code readable | Avoid surprises | Make code hard to misuse |
| ----------- | ----------- | ------ |
| **Make code modular** | **Make code reusable and generalizable** | **Make code testable and test it properly** |

**1. Make Code Readable**

- If our code has poor readability, other engineers will have to spend a lot of time trying to decipher it

**2. Avoid Surprises**

**3. Make Code Hard to Misuse**

**4. Make Code Modular**

- **Modularity** = object/system is composed of smaller components that can be independently exchanged or replaced (easily reconfigured)
- Beneficial to break a piece of code down into self-contained modules, where interactions between 2 adjacent modules happen in a single place and user a well-defined interface --> ensures the code will be easier to adapt to changing requirmeents (changing 1 thing doesn't require lots of change all over the place)
- Modular systems are easier to comprehend and reason about since functionality is broken into manageable chunks and interactions between chunks are well defined and documented --> increases chance that code will work

**5. Make Code Reusable and Generalizable**
| Reusability | Generalizability |
| ----------- | ----------- |
| Something can be used to solve the same problem but in multiple scenarios (same problem, different scenario) | Something can be used to solve multiple conceptually similar problems that are subtly different |

**6. Make Code Testable and Test it Properly**

- 3 different levels of testing
  | Unit Tests | Integration Tests | End-to-end (E2E) Tests|
  | ----------- | ----------- | ----------- |
  | Tests small units of code - ex. individual functions or classes (most commonly used) | Tests the integration of multiple components, modules and subsystems | Tests typical journey/workflow through a whole sofware system from start to finish |

- **Testability** = describes how well that code lends itself to being tested --> more modular code/systems are more testable
- Test-Driven Development: tests being written before the code

## 2. Layers of abstraction

- `null`: a value/reference/pointer being absent
  | Null is useful | Null is problematic |
  | ----------- | ----------- |
  | Concept of something being absent very often occurs | Not always obvious when a value can/cannot be null |

- **Null Safety/Void safety**: ensures that any variables/return values that can be null are marked as such and the compiler enforces that they are not used without first checking that they are not null

```c++
// SUPPORTS NULL SAFETY

// ? means that the return type can be null
Element? getFifthElement(List<Element> elements) {
  if (elements.size() < 5) {
    // null is returned when the value cannot be obtained
    return null;
  }
  return elements[4];
}
```

```c++
// DOESN'T SUPPORT NULL SAFETY

// Return type is an Optional Element
Optional<Element> getFifthElement(List<Element> elements) {
  if (elements.size() < 5) {
    return Optional.empty(); // Optional.empty() instead of null
  }
  return Optional.of(elements[4]);
}
```

Q. Why create layers of abstraction?

## 3. Other engineers and code contracts

## 4. Errors

# ii. IN PRACTICE

## 5. Make code readable

## 6. Avoid surprises

## 7. Make code hard to misuse

## 8. Make code modular

## 9. Make code reusable and generalizable

# iii. UNIT TESTING

## 10. Unit testing principles

## 11. Unit testing practices
