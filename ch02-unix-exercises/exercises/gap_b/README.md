# Shell Scripting: gap.sh 

First `unzip gapminder.zip` to get a `gapminder` directory. Write a bash script that will print out the files in the `gapminder` directory. Note that to be portable for testing purposes, you will need to use a **relative** path from the directory where the script lives (hint: start with `$PWD`). Your program will do the following:

* If there are no arguments, print out all the *basenames* of the files in sorted order
* If there is an argument, treat it like a regular expression and find files where the basename matches at the beginning of the string in a case-insensitive manner and print them in sorted order
* If no files are found, print a message telling the user 

````
$ ./gap.sh | head -5
     1	Afghanistan
     2	Albania
     3	Algeria
     4	Angola
     5	Argentina
$ ./gap.sh l
     1	Lebanon
     2	Lesotho
     3	Liberia
     4	Libya
$ ./gap.sh [w-z]
     1	West_Bank_and_Gaza
     2	Yemen_Rep
     3	Zambia
     4	Zimbabwe
$ ./gap.sh x
There are no countries starting with "x"

````

# Testing

You have been provided a `Makefile` that will run a test suite. This is what it should look like when all tests are passing:

````
$ make test
pytest -v test.py
============================= test session starts ==============================
platform darwin -- Python 3.6.8, pytest-4.2.0, py-1.7.0, pluggy-0.8.1 -- /anaconda3/bin/python
cachedir: .pytest_cache
rootdir: /Users/kyclark/work/python/practical_python_for_data_science/ch02-unix-exercises/exercises/gap_b, inifile:
plugins: remotedata-0.3.1, openfiles-0.3.2, doctestplus-0.2.0, arraydiff-0.3
collected 1 item

test.py::test_gap PASSED                                                 [100%]

=========================== 1 passed in 0.44 seconds ===========================
````
