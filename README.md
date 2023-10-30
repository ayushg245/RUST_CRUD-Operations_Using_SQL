[![Build binary release](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/release.yml/badge.svg)](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/release.yml)  [![Clippy](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/lint.yml/badge.svg)](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/lint.yml)  [![Rustfmt](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/rustfmt.yml/badge.svg)](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/rustfmt.yml)  [![Tests](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/tests.yml/badge.svg)](https://github.com/nogibjj/Individual_Project2_Ayush/actions/workflows/tests.yml)

## Goals
The goal of this project was to create a Rust repository that is able to create an SQLite databse, populate it with any csv document. I used a diabetes.csv found online and created a Diabetes.db for which i performed CRUD-operations. This project was created while adhering to DevOps principles, and is fully tested, linted, formatted, and built utilising Git-Hub Co-Pilot. A deeper explanation of the project, and how to run it, is explained below.

## Github Co-Pilot
I utilised the functionality of github co-pilot and the ability to transform code into different packages. The generative AI tool was able to help produce code in rust syntax with ease, Co-Pilot was also able to guide my syntax to produce code which was reproducible in Rust.

## Instructions

To inititalize the environment that has the requried packages and settings, COdespaces were used to execute the codes. 

The ``main.rs`` file accepts the commands via ``CLI``, the CLI are of the form:

```console
cargo run XX
```
Where 'XX' is the arguments for the file.

if only cargo run is entered, the file displays the prompts for the inputs it requires.

To manually Build the Optimized Rust Binary, execute the following command:
```console
cargo build --release
```

## C.R.U.D. Operations

The following below are screenshots that demonstrates that the code supports C.R.U.D operations (Create, Read, Update, Delete). All of them are SQL queries that were successfully executed. As well, I used Copilot to explain the different parts of functions that rusqlite required I used for query execution, as there wasn't a great explanation in the crate's documentation.

## Using RUST

Advantages of using Rust over Python:

1. Performance: Rust is faster and offers fine-grained memory control.
2. Memory Safety: Rust's ownership system ensures memory safety without a garbage collector.
3. Concurrency: Rust supports safe concurrency and is ideal for multi-threaded applications.
4. Predictable Performance: Rust avoids the GIL, providing more predictable performance.
5. Systems Programming: Rust is well-suited for tasks like operating systems and embedded systems.
6. Cross-Platform: Rust is cross-platform and works on various operating systems.
7. Strong Typing and Concurrency Guarantees: Rust's type system and concurrency guarantees reduce runtime errors.

## Create & Read

The code is able to create and read a table from the csv and create a data base for which queries can be run. 
From the image above we Select all columns from the database and produce a limit of 5 queries on the command line.

<img width="1069" alt="Screenshot 2023-10-27 at 4 41 56 PM" src="https://github.com/nogibjj/Individual_Project2_Ayush/blob/main/query1.png">

## Delete

The Outcome variable is `1` and `0` the query deletes the values with `0` which is an indication the patient doesnt have diabetes.
Below is the query ran as a command line tool.

<img width="1082" alt="Screenshot 2023-10-27 at 4 45 24 PM" src="https://github.com/nogibjj/Individual_Project2_Ayush/blob/main/query2.png">

# Update

The final query updates the Glucose column where it is `140` to `3000` and prints out the databse using the command line tool as seen below.

<img width="1059" alt="Screenshot 2023-10-27 at 4 49 12 PM" src="https://github.com/nogibjj/Individual_Project2_Ayush/blob/main/query_update.png">

## Contents

### 1. Rust_Binary
   A copy of the Optimized Rust Binary which is gerated when "cargo build --release" is executed.

### 2. README.md
   contains the information about the repository and instructions for using it
   

### 3. .github/workflows
   github actions are used to automate the following processes whenever a change is made to the files in the repository:
   - ``Build`` : creates the Optimized Rust Binary File
   - ``Copy`` : copies the binary file to the root directory of the repository as ``Rust_Binary`` for easier access
   - ``test`` : to test the main.rs file
   - ``format`` : uses ``rustfmt`` to format the python files
   - ``lint`` : uses ``clippy`` to lint the python files
   - ``upload and Download`` : Make the Github Action Rust binary atrifact downloadable
   

   
### 4. Makefile
   contains the instructions and sequences for the processes used in github actions and .devcontainer for creating the virtual environment
   
### 5. .devcontainer
   contains the ``dockerfile`` and ``devcontainer.json`` files which are used to build and define the setting of the virtual environment (codespaces - python) for running the codes.

### 6. Data
   a sample Dataset of [blood-pressure from Github](https://github.com/Opensourcefordatascience/Data-sets/blob/master/blood_pressure.csv) has been loaded into the resources folder and is used for testing.

### 7. resources 
   contains additonal files which are used in the README


## Demo Video
https://youtu.be/9ivxYCZ58q4
