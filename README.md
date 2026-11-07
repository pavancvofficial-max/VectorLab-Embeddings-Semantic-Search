# VectorLab — Embeddings & Semantic Search

A 45-minute interactive learning experience for beginners. It explains how text embeddings represent language as vectors, how cosine similarity compares vectors, and how semantic retrieval can find relevant information when exact keywords differ.

## Run locally

1. Extract the ZIP archive.
2. Open a terminal in the extracted folder.
3. Run `python -m http.server 8000`.
4. Visit `http://localhost:8000` in a modern browser.
5. Allow the pretrained embedding model to load. The first load requires an internet connection.

Opening `index.html` directly with `file://` may prevent browser modules from loading, so use the local server.

## Learning journey (45 minutes)

1. Why keyword search is not enough (5 min)
2. Embeddings, model pipeline, vectors and cosine similarity (10 min)
3. Semantic search playground (10 min)
4. Similarity calculator and limitations (7 min)
5. Hands-on challenge (6 min)
6. RAG and real-world applications (4 min)
7. Knowledge check (3 min)

The theory panels in the concept section are optional deeper reading. They cover Transformer encoders, pooling, contrastive-learning intuition, dense vs sparse retrieval, vector indexes, chunking and retrieval evaluation. For a 45-minute session, learners should focus on the core explanations and open deeper panels as time allows.

## Technology

- HTML, CSS and JavaScript
- Transformers.js
- `Xenova/all-MiniLM-L6-v2` pretrained sentence embedding model
- Mean pooling and L2 normalization
- Cosine similarity

The app runs the embedding model in the browser. It does not require a Python backend or an API key. Model files are downloaded from the configured model source at runtime.

## Important technical notes

- The model produces 384-dimensional sentence vectors. The UI shows the first 12 values for illustration, not the complete vector.
- The app normalizes embeddings, so the dot product between two returned vectors equals cosine similarity.
- Cosine similarity is a ranking signal, not a probability or a percentage of semantic overlap.
- The keyword baseline is a deliberately simple token-overlap demonstration, not BM25.
- Embedding similarity can miss negation, fine-grained distinctions, domain-specific meaning and factual correctness. Production systems should evaluate retrieval and may combine dense retrieval with keyword search, filters or reranking.

## Explanation video outline

1. Explain the learning problem: keyword mismatch.
2. Define an embedding and show the vector demonstration.
3. Explain the simplified encoder → pooling → vector pipeline.
4. Demonstrate semantic vs keyword retrieval.
5. Compare sentence similarity and discuss negation as a limitation.
6. Walk through the challenge and quiz.
7. Connect retrieval to RAG and real applications.
8. Explain why the lesson is structured from intuition to theory, experiment and application.

## Suggested checks before submission

- Test model loading on the browser and network you will use for the recording.
- Try every search preset, comparison preset, challenge hint, quiz option and quiz retake.
- Confirm the page is readable on a laptop and mobile-width screen.
- Record the explanation video after the live demonstration has been tested.
