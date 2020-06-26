# openmainframe-getting-started

Let's try some COBOL! This README contains the notes I'm taking while doing the course.

# Some basic stuff

Program Hierarchy::

    Division
      - Section
          - Paragrph
              - Sentence
                  - Statement

## Most important reserved words

These change *control flow*::

    EVALUATE
    PERFORM
    IF, THEN, ELSE
    
These change *data*::

    MOVE
    COMPUTE

## The four Divisions

Here's where you really recognize COBOL's age. Allocation at runtime? Nope.
Nice syntax? Nooope. Well, this is really a consequence of choosing businessy
people as COBOL's "target audience". I guess the actuall audience is a bit
different now. ^^

### IDENTIFICATION DIVISION

Meta information about the program (name, author, etc.)

### ENVIRONMENT DIVISION

Config, inputs, outputs. What I'd expect from the term "environment". :)

### DATA DIVISION

Can contain a FILE SECTION for input-calculate-output programs.

Can contain a LINKAGE SECTION for defining data from another program.
(Could this be described as a kind of "import ..." for *data* instead of *code*?

Can contain a LOCAL-STORAGE SECTION for data that is lost at
the end of the program.
(Comparable to the heap in C/C++/Java?)

Can contain a WORKING-STORAGE SECTION for keeping data for the program's lifetime.
(Something like a "persistent heap"?)

### PROCEDURE DIVISION

The actual code that is executed! The magic/number crunching happens here!

