# C++23 Template

A modern C++ project template with C++23 modules support.

## What should you change?

1. **Project name in `CMakeLists.txt`**:
   - Line 2: `project(cpptemplate LANGUAGES CXX)` → `project(yourproject LANGUAGES CXX)`
   - Line 21: `add_library(cpptemplate SHARED)` → `add_library(yourproject SHARED)`
   - Line 33: `set_target_properties(cpptemplate PROPERTIES` → `set_target_properties(yourproject PROPERTIES`
   - Line 42: `TARGET cpptemplate POST_BUILD` → `TARGET yourproject POST_BUILD`

2. **Module name in `src/cpptemplate.cppm`**:
   - Line 4: `export module cpptemplate;` → `export module yourmodule;`
   - Rename file: `cpptemplate.cppm` → `yourmodule.cppm`

3. **Import statement in `examples/*.cpp`**:
   - Line 1: `import cpptemplate;` → `import yourmodule;`

4. **Library link in `examples/CMakeLists.txt`**:
   - Line 15: `target_link_libraries(${EXAMPLE_NAME} PRIVATE cpptemplate)` → `target_link_libraries(${EXAMPLE_NAME} PRIVATE yourproject)`

5. **This README.md**: Update the title and description

## Build

```bash
just          # debug build
just release  # release build
```

## Run example

```bash
./bin/examples/hello
```
