# Refactoring reference

From "Refactoring: Improving the Design of Existing Code" by Martin Fowler

## Code Stinks

### Duplicated Code

Same code structure in more than one place.

__Possible approaches__:

_Same class_
* [Extract Method](#extract-method)

_Sibling subclasses_
* [Extract Method](#extract-method)
* [Pull Up Method](#pull-up-method)
* [Form Template Method](#form-template-method)
* [Substitute Algorithm](#substitute-algorithm)

_Unrelated classes_
* [Extract Class](#extract-class) 

### Long Method

Each method should perform only one task and be limited to a handful of lines.

__Possible approaches__:

* [Extract Method](#extract-method)
* [Replace Temp with Query](#replace-temp-with-query)
* [Introduce Parameter Object](#introduce-parameter-object) (if long parameter list)
* [Preserve Whole Object](#preserve-whole-object)
* [Replace Method with Method Object](#replace-method-with-method-object)
* [Decompose Conditional](#decompose-conditional)

### Large Class

"If a class is trying to do too much, it often shows up as too many instance variables."

__Possible approaches__:

* [Extract Class](#extract-class)
* [Extract Subclass](#extract-subclass)
* [Extract Interface](#extract-interface)
* [Duplicate Observed Data](#duplicate-observed-data)

### Long Parameter List

Long parameter lists are hard to understand and make a method difficult to use.

### Divergent Change

Components should have a single responsibility and should have a clear point in the system to make a necessary change.

### Shotgun Surgery

Whenever one type of change requires a lot of little changes in several places.

### Feature Envy

When a method of a class is more interested in a another class than the one it is in.
 
### Data Clumps

Bunches of several data elements that appear together in several places should be made into their own object.

### Primitive Obsession

Preferring primitive data types instead of creating small typed data objects, like zip code or phone number.

### Switch Statements

Usually switch statements hint at a need/opportunity for polymorphism.

### Parallel Inheritance

Special-case of shotgun surgery when creating a subclass of one class requires the creation of a subclass of another.

### Lazy Class

When a class isn't doing enough to "pay for itself" it should be eliminated.

### Speculative Generality

Creating hooks or "machinery" to allow for potential, future extension or features. If it isn't needed now, it isn't needed. Usually identified by classes only used by test cases.

### Temporary Field

Instance variables that are only used in certain circumstances.

### Message Chains

"You see message chains when a client asks one object for another object, which the client then asks for yet another object, which the client then asks for yet another another object, and so on." 

### Middle Man

Delegation is good but when more than half of the methods are delegating to another object then it is time to "remove the middle man".

### Inappropriate Intimacy

When classes know too much about other's internal workings.

### Alternative Classes with Different Interfaces

When classes provide alteratives of the same functionality but expose different interfaces.

### Incomplete Library Class

When there are features missing from library classes, which can't be changed.

### Data Class

Classes that just hold data and have getters and setters should "grow up" and take more responsibility.

### Refused Bequest

When a subclass doesn't need to use or implement 

### Comments

Comments aren't bad in themselves but they often indicate code that is more complicated than it should be. Comments often appear to describe sections of code that should be pulled out into their own method.

## Refactorings

### Add Parameter

### Change Birirectional Association to Unidirectional

### Change Reference to Value

### Change Unidirectional Association to Bidirectional

### Change Value to Reference

### Collapse Hierarchy

### Consolidate Conditional Expression

### Consolidate Duplicate Conditional Fragments

### Convert Procedural Design to Objects

### Decompose Conditional

### Duplicate Observed Data

### Encapsulate Collection

### Encapsulate Downcast

### Encapsulate Field

### Extract Class

### Extract Hierarchy

### Extract Interface

### Extract Method

### Extract Subclass

### Extract Superclass

### Form Template Method

### Hide Delegate

### Inline Class

### Inline Method

### Inline Temp

### Introduce Assertion

### Introduce Explaining Variable

### Introduce Foreign Method

### Introduce Local Extension

### Introduce Null Object

### Introduce Parameter Object

### Move Field

### Move Method

### Parameterize Method

### Preserve Whole Object

### Pull Up Constructor Body

### Pull Up Field

### Pull Up Method

### Push Down Field

### Push Down Method

### Remove Assignments to Parameters

### Remove Control Flag

### Remove Middle Man

### Remove Parameter

### Remove Setting Method

### Rename Method

### Replace Array with Object

### Replace Conditional with Polymorphism

### Replace Constructor with Factory Method

### Replace Data Value with Object

### Replace Delegation with Inheritance

### Replace Error Code with Exception

### Replace Exception with Test

### Replace Inheritance with Delegation

### Replace Magic Number with Symbolic Constant

### Replace Method with Method Object

### Replace Nested Conditional with Guard Clauses

### Replace Parameter with Explicit Methods

### Replace Parameter with Method

### Replace Record with Data Class

### Replace Subclass with Fields

### Replace Temp with Query

### Replace Type Code with Class

### Replace Type Code with State/Strategy

### Replace Type Code with Subclass

### Self Encapsulate Field

### Separate Domain from Presentation

### Separate Query from Modifier

### Split Temporary Variable

### Substitute Algorithm

### Tease Apart Inheritance
