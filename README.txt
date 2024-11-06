# RISCV-32I-Implementation

--------------------------------------------------------
A C++ implementation of RISCV-32I Processor
--------------------------------------------------------

Table of contents:

1. Directory structure
2. How to build
3. How to execute
4. How to view output/GUI

Directory Structure
-------------------

RISCV-32I-Implementation
  |
  |- bin
    |- RISCV
    |- Data Memory.mc
  |- doc
    |- Design Doc.docx
  |- include
    |- Core.h
    |- CacheFile.h
    |- GUI.h
    |- Pipeline.h
    |- RISCV.h
  |- src
    |- Core.cpp
    |- CacheFile.cpp
    |- GUI.cpp
    |- Pipeline.cpp
    |- main.cpp
    |- Makefile
    |- RISCV.cpp
  |- test
    |- array_sum.s
    |- array_sum.mc
    |- bubblesort.s
    |- bubblesort.mc
    |- fibonacci.s
    |- fibonacci.mc
    |- LFU.s
    |- LFU.mc
  |- gui
    |- public
      |- index.html
      |- styles.css
    |- src
      |- App.jsx
      |- index.js
      |- components
        |- filedata.json

How to build
------------

For compiling:
  $cd src
  $make

For cleaning the project:
  $cd src
  $make clean

How to execute
--------------

Command to execute program:
../bin/RISCV <knobs>

<knobs> --
          | -test <filename.mc>
          | -n <value of N>
          | -pipeline
          | -forward
          | -trace [<instruction number>]
          | -registers
          | -h (or) -help

(compulsory knob: -test <filename.mc>)
(all other knobs are optional:
          | -h (or) -help will show how to execute
          | default value of N is 5
          | default setting of pipelining, forwarding, tracing, and showing register values is off
          | if forward/trace is called without calling pipeline, it doesn't do anything
          | providing instruction number after -trace knob will activate tracing for that particular instruction only, otherwise for all instructions
          | -registers knob will show values in register file after every cycle)

How to view output/GUI
----------------------

All data memory is stored in file ../bin/Data Memory.mc

Run the following commands to view GUI:
$cd ../gui
$npm i react-scripts
$npm start