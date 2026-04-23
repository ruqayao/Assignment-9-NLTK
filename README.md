# Assignment-9-NLTK
# Purpose
The purpose of this assignment is to perform a comparative linguistic analysis on four unstructured text files. By applying Natural Language Processing (NLP) techniques, we aim to identify the underlying subject matter of the first three texts and use stylistic markers (trigrams) to determine which author likely wrote the fourth text.
# Dataset Requirements
- Input Files: The program requires four .txt files: RJ_Lovecraft.txt, RJ_Tolkein.txt, RJ_Martin.txt, and Martin.txt.
- Format: Plain text with standard UTF-8 encoding.
- Content: The texts are stylistic adaptations of the same story (Texts 1-3) and a standalone piece (Text 4).
# Class Design & Implementation
The project uses a single class, TextAnalyzer, to encapsulate all NLP logic:
- _init_(file_path): Sets up the instance and loads the raw data.
- load_text(): Handles file I/O.
- process_tokens(): Cleans data by removing "noise" (stopwords/punctuation) and normalizes words via stemming and lemmatization.
- get_top_tokens(n): Calculates frequency distributions to find the most significant words.
- count_named_entities(): Uses Part-of-Speech (POS) tagging and chunking to identify proper nouns like names and places.
- get_ngrams(n): Extracts sequences of n words to capture the "voice" or "style" of the author.
# Limitations
- Lexicon Size: Small text samples may lead to skewed frequency results where common words like "said" dominate.
- NER Accuracy: NLTK’s default ne_chunk can occasionally misidentify capitalized words at the start of sentences as entities.
- N-gram Overlap: In very short texts, most trigrams may only appear once, making statistical comparison difficult without larger datasets.
