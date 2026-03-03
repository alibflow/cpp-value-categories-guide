# 📘 C++ Value Categories — Visual Study Guide

> A comprehensive, beginner-friendly PDF guide to understanding **lvalue**, **prvalue**, and **xvalue** in modern C++ — with move semantics, perfect forwarding, copy elision, and comparisons with Rust, Python & Java.

---

## 🗂 What's Inside

The guide covers **12 sections** in a dark-themed, pedagogical PDF format:

| # | Section | Topics |
|---|---------|--------|
| 01 | **Why does it matter?** | Move semantics, perfect forwarding, copy elision |
| 02 | **Glossary** | 18 technical terms explained in plain language |
| 03 | **Taxonomy** | Visual diagram of all 5 value categories |
| 04 | **lvalue** | Named entities, stable identity, classic pitfalls |
| 05 | **prvalue** | Pure values, temporary materialization, RVO |
| 06 | **xvalue** | `std::move` internals, use-after-move danger |
| 07 | **glvalue & rvalue** | The two super-categories explained |
| 08 | **Move Semantics** | Copy vs move constructors, Rule of Five |
| 09 | **Perfect Forwarding** | `std::forward`, universal references, reference collapsing |
| 10 | **decltype & parentheses** | The subtle `return (x)` vs `return x` trap |
| 11 | **Other languages** | Rust ownership, Python references, Java/C# comparison |
| 12 | **Quiz + Cheat Sheet** | 6 annotated questions + express recap table |

---

## 📥 Download

👉 **[cpp_value_categories_guide.pdf](./cpp_value_categories_guide.pdf)**

---

## 🧠 Who Is This For?

- Developers **learning C++** who want to understand value categories properly
- Experienced programmers coming from **Python, Java, or Rust** looking for cross-language context
- Anyone preparing for a **C++ technical interview**
- Developers who want to understand **why** `std::move` works the way it does

---

## 🔑 Key Concepts Covered

```
lvalue    →  Has identity, not movable   (e.g. named variables)
prvalue   →  No identity, movable        (e.g. literals, temporaries)
xvalue    →  Has identity, movable       (e.g. std::move(x))
glvalue   →  lvalue ∪ xvalue            (anything with identity)
rvalue    →  prvalue ∪ xvalue           (anything movable)
```

---

## 💡 The Core Intuition

Instead of thinking "left side / right side of `=`", think in terms of two independent questions:

1. **Does this expression have a stable memory address?** → *Identity*
2. **Can we steal its internal resources?** → *Movability*

Every C++ expression answers these two questions — and that determines everything about how the compiler handles copies, moves, and optimizations.

---

## 🛠 Built With

- Python + [ReportLab](https://www.reportlab.com/) for PDF generation
- C++11 / C++14 / C++17 / C++23 standard references
- Examples tested with GCC and Clang

---

## 📄 License

MIT — feel free to share, adapt, and redistribute with attribution.
