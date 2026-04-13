# DFA Minimizer

A web-based application for minimizing Deterministic Finite Automata (DFA) using the Myhill–Nerode theorem and equivalence partitioning. The tool provides an interactive interface to define a DFA, visualize its structure, and observe the minimization process step by step.

## Live Demo

Access the application here:
https://pranavsinghtehlan.github.io/dfa-minimizer/

## Overview

This project is designed to assist in understanding and applying DFA minimization techniques. Users can input a custom automaton and obtain both the original and minimized versions, along with detailed intermediate steps.

## Features

* Interactive DFA input (states, alphabet, transitions, start state, accepting states)
* Automatic removal of unreachable states
* Step-by-step equivalence partitioning
* Visualization of original and minimized automata
* Graphical representation using SVG
* Generated transition table for minimized DFA
* Clean and responsive user interface with dark mode support

## Example Input

Use the following example to test the application:

* **States**: `q0, q1, q2, q3, q4, q5`
* **Alphabet**: `0, 1`
* **Start State**: `q0`
* **Accepting States**: `q2, q4, q5`

**Transitions:**

```
q0,0,q1
q0,1,q3
q1,0,q2
q1,1,q4
q2,0,q2
q2,1,q2
q3,0,q4
q3,1,q2
q4,0,q5
q4,1,q5
q5,0,q4
q5,1,q4
```

## Algorithm

The minimization process follows standard DFA minimization principles:

1. **Remove Unreachable States**
   States not reachable from the start state are eliminated.

2. **Initial Partitioning**
   States are divided into accepting and non-accepting groups.

3. **Partition Refinement**
   Groups are iteratively refined based on transition behavior until stable partitions are reached.

4. **Construct Minimized DFA**
   Each equivalence class becomes a single state in the minimized automaton.

## Project Structure

```
dfa-minimizer/
│── index.html      # Main application (UI + logic)
│── README.md       # Documentation
```

## Technologies Used

* HTML5
* CSS3 (with light/dark theme support)
* Vanilla JavaScript

## Use Cases

* Learning automata theory concepts
* Visualizing DFA minimization
* Academic demonstrations and assignments
* Quick validation of DFA designs

## Future Enhancements

* Export DFA as image or JSON
* Support for NFA to DFA conversion
* Improved visualization for large automata
* Step-by-step animation of transitions
