# BST Vocabulary Search Engine

A multi-threaded vocabulary search engine built in Java that uses a Binary Search Tree (BST) for indexing vocabulary words and supports word frequency analysis across multiple input files.

## Overview

This application builds a Binary Search Tree from a vocabulary file and processes multiple input files concurrently using Java threads. Users can search for words, view their frequency across documents, and explore the BST structure.

## Features

- **Binary Search Tree** — Efficient word storage with in-order traversal and search
- **Multi-threaded Processing** — Vocabulary and input files processed in parallel using Java threads
- **Word Frequency Analysis** — Count occurrences of words across input files
- **Interactive Menu** — Command-line interface for querying the indexed data
  - Display BST contents (in-order traversal)
  - Display vectors from input files
  - View matched words with frequency counts
  - Search queries across documents

## Tech Stack

- **Language:** Java
- **Data Structures:** Binary Search Tree, ArrayList, Vector
- **Concurrency:** Java Threads with `join()` synchronization

## Project Structure

```
.
├── DriverClass.java        # Main entry point with menu system
├── BinarySearchTree.java   # BST implementation (insert, search, traverse)
├── vocabulary.java         # Vocabulary file processor (Thread)
├── word.java               # Word frequency tracker
├── input1.java             # Input file processor (Thread)
├── vocabulary.txt          # Sample vocabulary file
├── input1.txt              # Sample input file 1
└── input2.txt              # Sample input file 2
```

## Usage

```bash
javac *.java
java i192015_A3.DriverClass vocabulary.txt input1.txt input2.txt
```

### Menu Options

1. Display BST built from vocabulary file
2. Display vectors built from input files
3. View matched words and their frequency
4. Search a query across documents
5. Exit

## How It Works

1. The vocabulary file is loaded into a BST in a separate thread
2. Each input file is processed in its own thread concurrently
3. All threads are synchronized using `join()` before the interactive menu starts
4. Users can query the indexed data through the menu system

## License

This project was developed as part of an Advanced Programming course assignment.
