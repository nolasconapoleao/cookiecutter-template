# {{cookiecutter.project_name}}

{{cookiecutter.project_short_description}}

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them

```
clang-format
cmake
doxygen
gcov
lcov
```

### Building and running

1. Run the cmake project and output the make recipe in the build folder
```
mkdir -p build/linux
cd build/linux
cmake -DCOMPILE_FOR_NON_UNIX:BOOL=OFF ../..
```

2. Build the library and all the executables defined in the Cmake 
```
make ${Project}
```

3. Run the game in the console
```
./${Project}
```

### Building and running in windows
In order to compile this game as an exe, use MinGW.

1. Install MinGW (Instructions in): 
http://www.mingw.org/wiki/getting_started

```
mkdir -p build/windows
cd build/windows
cmake -DCOMPILE_FOR_NON_UNIX:BOOL=ON -DCMAKE_BUILD_TYPE=Release ../..
```

2. Build the library and all the executables defined in the Cmake
```
make ${Project}
```

3. Run the game in the console
```
wine64 ${Project}.exe
OR double click it if you are in windows
```

### And coding style tests

In order to merge to master the code in the pull request should be formatted using the checks defined in <project>/.clang-format. To run the clang-format use:
```
clang-format -i $file
```

Another way is to use automatic formatting.
```
cd <project-path>
cp tools/pre-commit.sh .git/hooks/pre-commit
chmod +x .git/hooks/pre-commit
```

## Authors
* **{{cookiecutter.full_name}}** - *Initial work* - [{{cookiecutter.github_username}}]({{cookiecutter.email}})