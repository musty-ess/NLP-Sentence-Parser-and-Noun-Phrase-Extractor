# NLP Sentence Parser and Noun Phrase Extractor

## Overview

This project involves building an AI tool that parses sentences and extracts noun phrases using Python 3.12. The parser utilizes a context-free grammar to break down sentences into their structural components, helping to understand the sentence’s structure. Specifically, it focuses on identifying noun phrase chunks—parts of the sentence that function as noun phrases but do not contain other noun phrases inside them.

### Example Output

When provided with the sentence "Holmes sat", the parser generates the following structure:
```bash
      S
 _____|___
NP        VP 
|         |
N         V
|         | 
holmes   sat
```

## Background

Parsing is a fundamental task in Natural Language Processing (NLP). By determining the structure of sentences, computers can better understand their meanings and extract useful information, such as noun phrases. Noun phrases (NPs) help identify important subjects in sentences, and these structures are essential for a range of applications, including information retrieval, sentiment analysis, and question-answering systems.

In this project, we utilize context-free grammar (CFG) to represent the structure of sentences. The grammar is defined using a set of rules that can transform symbols into other symbols. Our aim is to develop a parser that can handle both simple and complex noun phrases.

## Features
1. **Sentence Parsing**:
   - Uses a context-free grammar to parse sentences.
   - Identifies sentence structure, breaking it down into noun phrases (NP), verbs (V), and other components.

2. **Noun Phrase Chunk Extraction**:
   - Extracts and prints all noun phrase chunks from the parsed sentences.
   - Noun phrases are substructures that represent the subjects or key elements in the sentence.

## Getting Started

- **Python 3.12**
- **NLTK library**: Used for tokenization and tree structure manipulation.
- **Clone the repo**: `git clone`  
- **Install dependencies using**: `pip install -r requirements.txt`
- **Run the program**: `python parser.py`. When prompted, input a sentence or provide a file path to a sentence file for the parser to process.  

## Project Structure

- **parser.py**: The main Python script that handles sentence parsing and noun phrase extraction.
- **sentences/**: Contains text files with sample sentences to parse.
- **requirements.txt**: Dependencies required for the project (NLTK library).

## Implementation Details

- **Context-Free Grammar**: The parser is based on context-free grammar rules that specify how different components of a sentence (such as noun phrases and verb phrases) are constructed. The `NONTERMINALS` global variable defines the grammar rules for non-terminal symbols, while `TERMINALS` defines the rules for terminal symbols (words).

- **Preprocessing**: The `preprocess` function tokenizes sentences into words, removes any non-alphabetic tokens, and converts everything to lowercase for uniformity.

- **Noun Phrase Chunking**: The `np_chunk` function identifies noun phrase chunks in the parsed sentence tree. It returns all NP chunks that do not contain other NP subtrees, helping isolate the key subjects in the sentence.

## Conclusion

This parser helps analyze sentence structure and identify important noun phrases, which can be crucial for many NLP tasks. By using context-free grammar and noun phrase chunking, we can better understand the subjects of a sentence and how they relate to other parts of the sentence.
