

---

# Inheritance in C++

## 📚 **Aim**

To study different types of inheritance in C++ — **single**, **multiple**, **multilevel**, and **hierarchical inheritance** — and understand the role of **access specifiers**.

## 🛠 **Tools**

* GNU g++ compiler for local compilation
* Any online C++ compiler

---

## 📝 **Theory**

In **Object-Oriented Programming**, **inheritance** is the process of creating new classes from existing ones.

* The existing class is the **base (parent) class**.
* The new class is the **derived (child) class**.

Inheritance:

* Promotes **code reusability**.
* Reduces **duplication**.
* Establishes **relationships** between classes.

Derived classes automatically include the base class’s members (except constructors, destructors, and private members).

### **Types of Inheritance in C++**

* **Single Inheritance** – One base class, one derived class.
* **Multiple Inheritance** – Derived class inherits from two or more base classes.
* **Multilevel Inheritance** – A class is derived from another derived class (forming a chain).
* **Hierarchical Inheritance** – Multiple classes derived from a single base class.

### **Access Specifiers**

* **Public** – Accessible everywhere.
* **Private** – Accessible only inside the class where it is defined.
* **Protected** – Accessible inside the base class and derived class, but not outside.

---

## **Syntax Examples**

### Single Inheritance

```cpp
class Base {
    // base class members
};

class Derived : public Base {
    // derived class members
};
```

### Multiple Inheritance

```cpp
class Base1 { };
class Base2 { };

class Derived : public Base1, public Base2 {
    // derived class members
};
```

### Multilevel Inheritance

```cpp
class Base { };

class Intermediate : public Base { };

class Derived : public Intermediate { };
```

### Hierarchical Inheritance

```cpp
class Base { };

class Derived1 : public Base { };
class Derived2 : public Base { };
class Derived3 : public Base { };
```

### Access Specifiers

```cpp
class Base {
public:
    int publicVar;
protected:
    int protectedVar;
private:
    int privateVar;
};

class Derived : public Base {
    // publicVar → public
    // protectedVar → protected
    // privateVar → not accessible
};
```

---

## 💻 **Programs**

### **Program 1: Single Inheritance**

**Logic:** Demonstrates single inheritance using a `Student` base class and `Test` derived class.
**Algorithm:**

1. Define `Student` with roll and name.
2. Define `Test` derived from `Student`.
3. Add marks and display total marks & percentage.
4. In `main()`, create object of `Test` and display details.

---

### **Program 2: Multiple Inheritance**

**Logic:** Demonstrates multiple inheritance with `SmartPhone` inheriting from `Brand` and `Features`.
**Algorithm:**

1. Define `Brand` with brand name.
2. Define `Features` with calling() and messaging().
3. Define `SmartPhone` inheriting from both.
4. Add model and display in `main()`.

---

### **Program 3: Multilevel Inheritance**

**Logic:** Demonstrates a chain of inheritance — `ElectricDevice` → `Computer` → `Laptop`.
**Algorithm:**

1. Base `ElectricDevice` with powerOn() and powerOff().
2. Derived `Computer` adds brand, processor, RAM, storage.
3. Derived `Laptop` adds battery life.
4. In `main()`, create and test objects.

---

### **Program 4: Hierarchical Inheritance**

**Logic:** Shows multiple derived classes sharing one base `Circuits`.
**Algorithm:**

1. Base `Circuits` with on() and off().
2. Derived `Clipper` and `Clamper`.
3. Further derive `seriesClipper`, `parallelClipper`, `positiveClamper`, `negativeClamper`.
4. Test all in `main()`.

---

### **Program 5: Access Specifiers**

**Logic:** Demonstrates how `public`, `protected`, and `private` members affect inheritance.
**Algorithm:**

1. Base `ElectricDevice` with public, protected, private members.
2. Derived `Computer` and `Laptop` show access differences.
3. Test access in `main()`.

---

## ✅ **Conclusion**

Inheritance in C++ allows classes to **reuse** and **extend** functionality of other classes:

* **Single inheritance** links one base to one derived class.
* **Multiple inheritance** combines features from multiple classes.
* **Multilevel inheritance** forms a chain.
* **Hierarchical inheritance** shares one base across many derived classes.

Access specifiers control **visibility and accessibility** of class members. Overall, inheritance leads to **cleaner**, **modular**, and **powerful** C++ programs.

---

