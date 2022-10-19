Demonstration of https://github.com/oneapi-src/oneTBB/issues/920. Code taken from the [official Getting Started example](https://oneapi-src.github.io/oneTBB/GSG/get_started.html#example).

The prebuilt oneTBB v2021.6.0 binary was created with Xcode 13.4.1 (Apple clang 13) in debug+static mode.

Build example:

```
cmake -S . -B build -G Ninja -D CMAKE_PREFIX_PATH=tbb-installed/lib/cmake
cmake --build build
```

Sample run invocation:

```
$ build/test_package
Assertion node(val).my_prev_node == &node(val) && node(val).my_next_node == &node(val) failed (located in the push_front function, line in file: 135)
Detailed description: Object with intrusive list node can be part of only one intrusive list simultaneously
```
