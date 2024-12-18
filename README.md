# Exploring the Limits of Retrieval-Augmented Generation (RAG) with Gemini and SentenceTransformers

This project demonstrates the use of **Retrieval-Augmented Generation (RAG)** techniques by leveraging **Gemini** for question-answering tasks and **SentenceTransformers** for generating high-quality embeddings. We explore the boundaries of RAG's capabilities by applying it to a knowledge base derived from a chess openings book.

---

## Overview

The project extracts semantic vectors from a text corpus (a chess openings book), generates embeddings using **SentenceTransformers**, and retrieves the most relevant context for a given user query. The relevant information is passed to the Gemini model to generate an accurate and context-aware response.

---

## Example Workflow

1. **Knowledge Base**: Extracted key insights and strategies from a chess openings book, with a focus on explaining moves, strategies, and common variations.
2. **Embedding Generation**: Transformed the extracted knowledge into embeddings using **SentenceTransformers** for efficient semantic search.
3. **Query Matching**: Embedded the user's question, retrieved the top-`k` most relevant passages, and provided this context to Gemini for response generation.

### Example Interaction

- **User Input**:  
  _"Tell me about the Ruy Lopez opening"_

- **Relevant Context Retrieved**:
Context 1:
    OPEN GAMES
    They start:
    1. e2-e4 e7-e5
    WHITE SAYS:
    You're expecting the Ruy Lopez? Tough. I'm going to
    play my favourite opening and see what you know
    about it. It could be anything from a wild gambit to a
    quiet line. You'll soon find out.
    BLACK SAYS:
    These openings really aren't so scary. I'm well
    prepared: I can reach at least an equal position
    whichever one you choose. Go ahead and do your
    worst.
    Most of these openings fall into one of three
    categories:
    1. White plays for a central break with d4 (Scotch Game,
    Ponziani, most lines of Giuoco Piano and Two Knights).
    2. White plays for a central break with f4 (King's Gambit,
    most lines of the Vienna and Bishop's Opening).
    3. White plays quietly with d3 (Giuoco Pianissimo, Spanish
    Four Knights).
    We also look at some other defences for Black after 2.
    Ng1-f3, from safe defensive systems to sharp counter-
    gambits. What should Black do next?Ideas for White:
    Adults will expect the Ruy Lopez while juniors are more used to this sort of opening.
    So it's a good idea to play the Ruy Lopez against juniors, and, for example, the Giuoco
    Piano against adults.

Context 2: 
    - 2. d2-d4 e5xd43. c2-c3 d4xc3
    4. Bf1-c4 c3xb2
    5. Bc1xb2 d7-d5THE RUY LOPEZ
    It starts:
    1. e2-e4 e7-e52. Ng1-f3 Nb8-c63. Bf1-b5
    WHITE SAYS:
    I'm going to attack your e-pawn and prevent you
    playing d5 to free your game. At the same time I'll
    set up a pawn centre with d4, perhaps after playing
    c3 first.
    BLACK SAYS:
    I'm going to defend my centre and play to reach anequal position. I'll make sure you don't take over all
    the centre and when you overreach I'll hit back and
    take the advantage.
    What happens next?
    The tactical battle over the next few moves revolves
    around the two e-pawns. The best way to explain
    this is to go through the most popular variation
    move by move.

- **Generated Response**:  
_"The Ruy Lopez is a classical chess opening where White aims to control the center and target Black's pawn structure, particularly focusing on the e5-pawn. Black’s main strategy is to defend and counterattack, often starting with moves like 3...a6 and 4...Nf6."_  

---

## Features

- **SentenceTransformers for Embeddings**:
- Pretrained SentenceTransformers models are used to encode the corpus and queries into dense vectors.
- Efficient similarity search to find top-`k` relevant documents.

- **Gemini for Text Generation**:
- Leverages retrieved context to provide accurate and detailed answers.
- Demonstrates RAG capabilities in generating natural language responses.

---

## Installation

1. Clone this repository:
 ```bash
 git clone https://github.com/your-repo/rag-exploration.git
 cd rag

