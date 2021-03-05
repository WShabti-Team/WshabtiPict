# WShabtiPict

A simple tool for combinatorial test cases and **JUnit5** code generation. 


## Building with clang++ on Linux, OS/X, *BSD, etc.
Install clang through your package manager (most systems), Xcode (OS/X), or from the [LLVM website](http://llvm.org/releases/).
On Linux, you also need to install recent libstdc++ offered by gcc 5.

Run `make` to build the `pict` binary.



```bash
make
```

## Building on Windows
Install [cygwin](http://www.cygwin.com/) and clone this repo into your home folder. Run `make` to build the `pict` binary.

## Usage Sample

```bash
./WShabtiPict
SourceCode Path: ClassExample/Calcolatrice.java

-----METHOD: public int somma(int a, int b)-----
#Do you want skip this method? (y/n)
Please specify your choice: n

#Do you want specify input file source? (y/n)
Please specify your choice: n

Please specify, separated by a comma, all possible values of "a"
For a range of numbers you can use the syntax "start:stop:step": 1:5:1,7

Please specify, separated by a comma, all possible values of "b"
For a range of numbers you can use the syntax "start:stop:step": 3,4

#Do you want specify Exclusive Constraints? (y/n)
Please specify your choice: y

To specify a combination to exclude, use the syntax "value1,value2,...".
Use "*" if you don't care about a parameter.

Please specify a combination to exclude or "stop" to terminate: 1,3

Please specify a combination to exclude or "stop" to terminate: *,4

Please specify a combination to exclude or "stop" to terminate: stop

Please specify the order of combinations for "somma": 2

-----ORACLE: public int somma(int a, int b)-----
Please specify the oracle for the following possible combinations
For a range of numbers you can use the syntax "expected_value:delta"
somma(2,3): 5
somma(4,3): 7
somma(3,3): 6
somma(5,3): 8
somma(7,3): 10

-----METHOD: public float divisione (int a, int b)-----
#Do you want skip this method? (y/n)
Please specify your choice: n

#Do you want specify input file source? (y/n)
Please specify your choice: y
Please specify the parameter file path: divisione_input.txt

Please specify the order of combinations for "divisione": 2

-----ORACLE: public float divisione (int a, int b)-----
Please specify the oracle for the following possible combinations
For a range of numbers you can use the syntax "expected_value:delta"
divisione(10,1): 10
divisione(20,3): 6:1
divisione(10,3): 3.3:0.2
divisione(5,2): 2.5
divisione(5,3): 1:1
divisione(5,1): 5
divisione(20,1): 20

Your tests have been generated, please check JUnitTests/Calcolatrice/
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
