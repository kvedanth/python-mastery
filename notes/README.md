# Python Advanced Concepts — Master Reference

A comprehensive, production-grade reference covering **55 advanced Python topics** — from virtual environments and exception handling to asynchronous programming, metaprogramming, and design patterns. Each topic is structured as a standalone deep-dive with simple, intermediate, and architect-level examples, common mistakes, best practices, testing strategies, and interview questions.

---

## How to Use This Reference

Each file follows a consistent structure:

| Section | Purpose |
|---|---|
| **Overview** | Concept definition and production context |
| **Why It Matters** | Mermaid diagrams showing the concept's impact chain |
| **Simple Example** | Beginner-friendly code with explanation and expected output |
| **Intermediate Example** | Real-world usage patterns |
| **Advanced / Architect-Level Example** | Production system design with trade-off analysis |
| **Common Mistakes** | Anti-patterns with corrected alternatives |
| **Best Practices** | Actionable guidelines |
| **Performance Considerations** | Benchmarks and optimization notes |
| **Testing Strategy** | pytest-based test examples |
| **Debugging Tips** | Tools and techniques for diagnosing issues |
| **Interview Questions** | Beginner → Intermediate → Architect-level Q&A |
| **Key Takeaways** | Concise summary bullets |
| **Mini Project Idea** | Hands-on project with folder structure and extension ideas |

---

## Topic Index

### Foundation & Environment

| # | Topic | Key Concepts |
|---|---|---|
| 01 | [Python Virtual Environments](01_Python%20Virtual%20Environments.md) | `venv`, `pip`, `pyproject.toml`, dependency isolation |
| 02 | [Exception Handling](02_Exception%20Handling.md) | `try/except/else/finally`, exception chaining, custom hierarchies |
| 03 | [Error and Exception Types](03_Error%20and%20Exception%20Types.md) | Built-in exception hierarchy, `BaseException`, `Exception` |
| 04 | [Custom Exceptions](04_Custom%20Exceptions.md) | Exception design, domain errors, error codes |
| 05 | [File I/O](05_File%20I-O.md) | `open()`, `pathlib`, context managers, binary/text modes |

### Type System & Annotations

| # | Topic | Key Concepts |
|---|---|---|
| 06 | [Bitwise Operations](06_Bitwise%20Operations.md) | `&`, `\|`, `^`, `~`, `<<`, `>>`, `IntFlag`, bitmasks |
| 07 | [Enumerations](07_Enumerations.md) | `Enum`, `IntEnum`, `StrEnum`, `Flag`, `auto()`, `@unique` |
| 08 | [Type Hints](08_Type%20Hints.md) | `list[T]`, `dict[K,V]`, `Optional`, `Union`, `Protocol`, `TypedDict` |
| 09 | [Function Annotation](09_Function%20Annotation.md) | `__annotations__`, `get_type_hints()`, `Annotated`, `inspect.signature()` |
| 10 | [Static Typing](10_Static%20Typing.md) | `mypy`, `pyright`, `--strict`, `py.typed`, `TYPE_CHECKING`, `cast()` |

### Functional Programming

| # | Topic | Key Concepts |
|---|---|---|
| 11 | [Closures](11_Closures.md) | Enclosing scope, `nonlocal`, `__closure__`, loop closure bug |
| 12 | [Lambda Functions](12_Lambda%20Functions.md) | Anonymous functions, `sorted(key=)`, dispatch tables, `operator` module |
| 13 | [Higher-Order Functions](13_Higher-Order%20Functions.md) | `map`, `filter`, `reduce`, `pipe`, `compose`, middleware chains |
| 14 | [Partial Functions](14_Partial%20Functions.md) | `functools.partial`, argument pre-filling, configuration factories |
| 15 | [Currying](15_Currying.md) | Single-argument chains, `toolz.curry`, point-free pipelines |
| 16 | [Functional Programming Paradigm](16_Functional%20Programming%20Paradigm.md) | Pure functions, immutability, `Result` monad, `frozen=True` |

### Decorators & Metaprogramming

| # | Topic | Key Concepts |
|---|---|---|
| 17 | [Decorators](17_Decorators.md) | `@wraps`, parameterized decorators, class-based decorators, async-aware |
| 18 | [Property Decorators](18_Property%20Decorators.md) | `@property`, `@cached_property`, custom descriptors, cache invalidation |
| 19 | [Magic Methods](19_Magic%20Methods.md) | Dunder methods, `__repr__`, `__eq__`, `__hash__`, `__enter__`/`__exit__` |
| 20 | [Operator Overloading](20_Operator%20Overloading.md) | `__add__`, `__matmul__`, `NotImplemented`, `@total_ordering`, DSLs |
| 21 | [Callable Objects](21_Callable%20Objects.md) | `__call__`, stateful callables, Strategy pattern, pipeline steps |
| 38 | [Monkey Patching](38_Monkey%20Patching.md) | Runtime modification, testing mocks, risks and safeguards |
| 39 | [Metaprogramming](39_Metaprogramming.md) | Metaclasses, `__init_subclass__`, `type()`, class decorators |
| 40 | [Dynamic Code Execution](40_Dynamic%20Code%20Execution%20(eval%2C%20exec).md) | `eval()`, `exec()`, `compile()`, security considerations |

### Object-Oriented Programming

| # | Topic | Key Concepts |
|---|---|---|
| 22 | [Data Classes](22_Data%20Classes.md) | `@dataclass`, `field()`, `frozen=True`, `__post_init__`, `asdict()` |
| 23 | [Duck Typing](23_Duck%20Typing.md) | Structural typing, `Protocol`, `isinstance()`, EAFP vs LBYL |
| 24 | [Multiple Inheritance](24_Multiple%20Inheritance.md) | MRO, `super()`, C3 linearization, diamond problem |
| 25 | [Mixins](25_Mixins.md) | Mixin design, composition over inheritance, `LoggingMixin` |
| 26 | [Abstract Base Classes (ABCs)](26_Abstract%20Base%20Classes%20(ABCs).md) | `ABC`, `@abstractmethod`, `register()`, virtual subclasses |
| 27 | [Name Mangling](27_Name%20Mangling.md) | `__name` → `_ClassName__name`, access control, subclass safety |
| 28 | [Function Overloading](28_Function%20Overloading.md) | `@overload`, `singledispatch`, `multipledispatch` |
| 34 | [Singleton Pattern](34_Singleton%20Pattern.md) | Metaclass singleton, module-level singleton, thread safety |

### Iterators, Generators & Coroutines

| # | Topic | Key Concepts |
|---|---|---|
| 29 | [Iterators](29_Iterators.md) | `__iter__`, `__next__`, `StopIteration`, iterator protocol |
| 30 | [Custom Iterators](30_Custom%20Iterators.md) | Stateful iterators, infinite sequences, chaining |
| 31 | [Generators](31_Generators.md) | `yield`, `yield from`, generator expressions, lazy evaluation |
| 32 | [Coroutines](32_Coroutines.md) | `send()`, `throw()`, `close()`, generator-based coroutines |
| 33 | [Memoization](33_Memoization.md) | `@lru_cache`, `@cache`, custom TTL cache, cache invalidation |

### Design Patterns & Architecture

| # | Topic | Key Concepts |
|---|---|---|
| 35 | [Design Patterns](35_Design%20Patterns.md) | Strategy, Observer, Factory, Builder, Chain of Responsibility, Command |
| 36 | [Context Managers](36_Context%20Managers.md) | `__enter__`/`__exit__`, `@contextmanager`, `contextlib`, resource management |
| 37 | [Context Variables](37_Context%20Variables.md) | `contextvars.ContextVar`, async context isolation, request-scoped state |

### Data & Serialization

| # | Topic | Key Concepts |
|---|---|---|
| 41 | [Serialization (Pickling, JSON)](41_Serialization%20(Pickling%2C%20JSON).md) | `pickle`, `json`, `__getstate__`/`__setstate__`, custom encoders |
| 42 | [Regular Expressions](42_Regular%20Expressions.md) | `re` module, groups, lookaheads, compiled patterns, `re.VERBOSE` |
| 43 | [Parsing (XML, JSON, HTML)](43_Parsing%20(XML%2C%20JSON%2C%20HTML).md) | `xml.etree`, `json`, `html.parser`, `lxml`, `BeautifulSoup` |
| 44 | [Data Structures (Linked Lists, Trees, Graphs)](44_Data%20Structures%20(Linked%20Lists%2C%20Trees%2C%20Graphs).md) | Custom implementations, `collections`, `heapq`, graph algorithms |
| 45 | [Algorithms (Sorting, Searching)](45_Algorithms%20(Sorting%2C%20Searching).md) | Sorting algorithms, binary search, complexity analysis |
| 46 | [Computational Geometry](46_Computational%20Geometry.md) | Convex hull, point-in-polygon, spatial algorithms |

### Concurrency & Parallelism

| # | Topic | Key Concepts |
|---|---|---|
| 47 | [Threading](47_Threading.md) | `threading.Thread`, `ThreadPoolExecutor`, GIL, daemon threads |
| 48 | [Synchronization (Locks, Semaphores)](48_Synchronization%20(Locks%2C%20Semaphores).md) | `Lock`, `RLock`, `Semaphore`, `Event`, `Condition`, deadlock prevention |
| 49 | [Multiprocessing](49_Multiprocessing.md) | `multiprocessing.Process`, `Pool`, `Queue`, `Pipe`, shared memory |
| 50 | [Parallel Processing](50_Parallel%20Processing.md) | `concurrent.futures`, `ProcessPoolExecutor`, `ThreadPoolExecutor` |
| 51 | [Asynchronous Programming](51_Asynchronous%20Programming.md) | `asyncio`, `async/await`, `gather`, `create_task`, `Semaphore`, `uvloop` |

### Networking, Testing & Tooling

| # | Topic | Key Concepts |
|---|---|---|
| 52 | [Networking (Sockets, HTTP)](52_Networking%20(Sockets%2C%20HTTP).md) | `socket`, `http.client`, `urllib`, `aiohttp`, TCP/UDP |
| 53 | [Debugging Techniques](53_Debugging%20Techniques.md) | `pdb`, `breakpoint()`, `logging`, `traceback`, profiling |
| 54 | [Testing Frameworks (pytest, unittest)](54_Testing%20Frameworks%20(e.g.%2C%20pytest%2C%20unittest).md) | `pytest`, fixtures, mocking, parametrize, coverage |
| 55 | [Packaging and Distribution](55_Packaging%20and%20Distribution.md) | `pyproject.toml`, `setuptools`, `wheel`, PyPI, `hatch` |

---

## Learning Paths

### Path 1: Python Fundamentals Reinforcement
Start here if you want to solidify core Python knowledge before advancing.

```
01 → 02 → 03 → 04 → 05 → 07 → 08 → 22 → 29 → 31
```

### Path 2: Functional Programming Mastery
Deep dive into Python's functional programming capabilities.

```
11 → 12 → 13 → 14 → 15 → 16 → 17 → 33
```

### Path 3: Object-Oriented Architecture
Master Python's OOP model from basics to advanced patterns.

```
19 → 20 → 21 → 22 → 23 → 24 → 25 → 26 → 18 → 34 → 35
```

### Path 4: Type Safety & Static Analysis
Build type-safe, statically-checked Python codebases.

```
08 → 09 → 10 → 07 → 23 → 26 → 28
```

### Path 5: Concurrency & Async Systems
Build high-performance concurrent Python applications.

```
47 → 48 → 49 → 50 → 51 → 32 → 37
```

### Path 6: Production Python Architecture
End-to-end path for senior engineers and architects.

```
10 → 17 → 18 → 22 → 35 → 36 → 37 → 39 → 51 → 54 → 55
```

### Path 7: AI/ML Systems Engineering
Focused path for building RAG pipelines and AI agent frameworks.

```
08 → 10 → 16 → 17 → 21 → 22 → 35 → 51 → 33 → 36
```

---

## Quick Reference: Key Patterns

### Decorator Factory (Parameterized Decorator)
```python
# 17_Decorators.md
from functools import wraps

def retry(max_attempts: int = 3, delay: float = 1.0):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            for attempt in range(max_attempts):
                try:
                    return func(*args, **kwargs)
                except Exception:
                    if attempt == max_attempts - 1:
                        raise
        return wrapper
    return decorator
```

### Immutable Data Class with Validation
```python
# 22_Data Classes.md
from dataclasses import dataclass

@dataclass(frozen=True)
class Config:
    host: str
    port: int
    timeout: float = 30.0

    def __post_init__(self):
        if not (1 <= self.port <= 65535):
            raise ValueError(f"Invalid port: {self.port}")
```

### Protocol-Based Structural Typing
```python
# 08_Type Hints.md, 23_Duck Typing.md
from typing import Protocol, runtime_checkable

@runtime_checkable
class Retriever(Protocol):
    def retrieve(self, query: str, top_k: int) -> list[dict]: ...
```

### Result Monad for Error Handling
```python
# 16_Functional Programming Paradigm.md
from dataclasses import dataclass
from typing import TypeVar, Generic, Callable

T = TypeVar("T")
U = TypeVar("U")

@dataclass(frozen=True)
class Ok(Generic[T]):
    value: T
    def map(self, f: Callable[[T], U]) -> "Ok[U] | Err":
        try:
            return Ok(f(self.value))
        except Exception as e:
            return Err(str(e))

@dataclass(frozen=True)
class Err:
    error: str
    def map(self, f: Callable) -> "Err":
        return self
```

### Async Pipeline with Semaphore
```python
# 51_Asynchronous Programming.md
import asyncio

async def process_all(items: list, max_concurrent: int = 5) -> list:
    semaphore = asyncio.Semaphore(max_concurrent)

    async def process_one(item):
        async with semaphore:
            return await do_work(item)

    return await asyncio.gather(*[process_one(i) for i in items])
```

### Custom Descriptor
```python
# 18_Property Decorators.md
class ValidatedField:
    def __set_name__(self, owner, name):
        self.name = name
        self.private = f"_{name}"

    def __get__(self, obj, objtype=None):
        if obj is None:
            return self
        return getattr(obj, self.private, None)

    def __set__(self, obj, value):
        if not isinstance(value, (int, float)) or value < 0:
            raise ValueError(f"{self.name} must be a non-negative number")
        setattr(obj, self.private, value)
```

### IntFlag Permission System
```python
# 06_Bitwise Operations.md
from enum import IntFlag, auto

class Permission(IntFlag):
    READ    = auto()  # 1
    WRITE   = auto()  # 2
    EXECUTE = auto()  # 4
    ADMIN   = READ | WRITE | EXECUTE

def has_permission(user_perms: Permission, required: Permission) -> bool:
    return bool(user_perms & required)
```

---

## Common Anti-Patterns to Avoid

| Anti-Pattern | Topic | Correct Approach |
|---|---|---|
| Mutable default arguments | 22 | Use `field(default_factory=list)` |
| Bare `except:` clause | 02 | Catch specific exception types |
| `__annotations__` instead of `get_type_hints()` | 09 | Use `get_type_hints()` for resolved types |
| Missing `@wraps` in decorators | 17 | Always use `@functools.wraps(func)` |
| `__eq__` without `__hash__` | 19, 20 | Define both or set `__hash__ = None` |
| Blocking I/O in async coroutines | 51 | Use `asyncio.to_thread()` |
| Loop closure bug with lambdas | 11, 12 | Use `lambda i=i: i` for capture by value |
| `type: ignore` without error code | 10 | Use `# type: ignore[specific-code]` |
| Singleton via global state | 34 | Use dependency injection instead |
| `eval()` on untrusted input | 40 | Use `ast.literal_eval()` or a safe parser |

---

## Technology Stack Referenced

| Category | Libraries / Tools |
|---|---|
| **Type Checking** | `mypy`, `pyright`, `beartype` |
| **Testing** | `pytest`, `pytest-asyncio`, `unittest.mock` |
| **Async HTTP** | `aiohttp`, `httpx` |
| **Data Validation** | `pydantic`, `attrs` |
| **Functional** | `toolz`, `cytoolz`, `returns` |
| **Serialization** | `pickle`, `json`, `msgpack`, `orjson` |
| **Concurrency** | `asyncio`, `threading`, `multiprocessing`, `concurrent.futures` |
| **Performance** | `uvloop`, `cython`, `numba` |
| **Packaging** | `hatch`, `setuptools`, `poetry`, `pip` |
| **AI/ML** | `langchain`, `llama-index`, `numpy`, `torch` |

---

## Interview Preparation Guide

### By Difficulty Level

**Beginner Topics** (1–2 years experience):
- Exception Handling (02), Type Hints (08), Decorators (17), Data Classes (22), Generators (31)

**Intermediate Topics** (3–5 years experience):
- Closures (11), Magic Methods (19), ABCs (26), Context Managers (36), Threading (47)

**Senior / Architect Topics** (5+ years experience):
- Static Typing (10), Metaprogramming (39), Design Patterns (35), Async Programming (51), Functional Programming (16)

### Most Frequently Asked Interview Topics

1. **Decorators** — How they work, `@wraps`, parameterized decorators
2. **Generators vs Iterators** — `yield`, lazy evaluation, memory efficiency
3. **GIL and Concurrency** — Threading vs multiprocessing vs asyncio
4. **Magic Methods** — `__repr__`, `__eq__`, `__hash__`, context managers
5. **Type System** — `Protocol`, `TypeVar`, `Generic`, mypy
6. **Closures** — `nonlocal`, loop closure bug, decorator implementation
7. **Data Classes** — `frozen=True`, `field()`, `__post_init__`
8. **Design Patterns** — Strategy, Observer, Factory in Python

---

## File Naming Convention

Files are numbered `NN_Topic Name.md` for easy ordering. Spaces in filenames use URL encoding (`%20`) in links above.

---

## Contributing

Each topic file follows the standard template defined in `prompts/PromptTemplate.txt`. When adding new topics:

1. Follow the established structure (Overview → Simple → Intermediate → Advanced → Mistakes → Best Practices → Performance → Testing → Debugging → Interview Questions → Key Takeaways → Mini Project → Final Summary)
2. Include Mermaid diagrams for the "Why It Matters" section
3. Ensure all code examples have expected output
4. Include architect-level examples with design trade-off tables
5. Add the topic to this README's index

---

*This reference is designed for Python developers at all levels — from those solidifying fundamentals to architects designing production AI and backend systems.*
