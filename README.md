# cake-c

A simple wrapper around CakeML to make compiling nicer.

---

## Why?

The traditional method for turning a CakeML program into an executable:

(Where both the ```cake``` executable and the ```basis_ffi.c``` file are provided by CakeML.)

```
> cake <myfile.cml > myfile.S
> cc -o myfile basis_ffi.c myfile.S
```

Using cake-c:

```
> cake-c myfile.cml myfile
```

---

## Installation

Place ```cake-c``` into the same directory as CakeML, and then make it available to your shell by either:

* Ensuring the CakeML directory is part of PATH
* Have an alias to ```cake-c```.

```cake-c``` doesn't care which option you go with.

---

## Usage

```cake-c``` does have commandline help in the form of: ```cake-c --help```.

```cake-c``` takes two arguments:

1. The name of the file you are compiling.
2. The name of the executable you wish to create.

```cake-c``` will place the executable in the same folder as the file you are compiling.

For example:

```
> echo 'print "Hello, World!\n";' > hello.cml
> cake-c hello.cml hello
Setting up environment...
Environment built.
Compiling CakeML data...
Compiling executable...
Done Compiling.
Removing environment...
Environment removed.
> ./hello
Hello, World!
```

---

## LICENSE

```cake-c``` is licensed under Creative Commons, Zero License.

It is effectively Public Domain, but the exact legal code can be found [here](LICENSE).
