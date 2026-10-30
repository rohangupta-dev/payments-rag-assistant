# payments-rag-assistant

AI assistant for real-time payments: retrieval-augmented answers over payment specs, flows and runbooks.

> 🚧 Work in progress. A learning project for TypeScript, Node.js and AWS serverless.

## Why

Payment engineers spend a lot of time searching specs, message formats and runbooks,
especially during incidents. This project tries a RAG (retrieval-augmented generation)
assistant that answers those questions and cites its sources.

## Planned architecture

```
Docs (specs, flows, runbooks)
        │  ingest + chunk + embed
        ▼
   Vector store ◄──── retrieve ──── Query API (AWS Lambda + API Gateway)
                                         │
                                         ▼
                                   LLM answer + citations
```

## Tech stack

- **Language:** TypeScript on Node.js
- **Runtime:** AWS serverless (Lambda, API Gateway)
- **AI:** embeddings, vector search and an LLM for grounded answers

## Roadmap

- [ ] Document ingestion and chunking pipeline
- [ ] Embeddings and vector store
- [ ] Query API on Lambda
- [ ] Answers with source citations
- [ ] Evaluation set of real payments questions

## Note

This project uses only public or synthetic documents. No bank or customer data.

## Author

Rohan Gupta · [LinkedIn](https://www.linkedin.com/in/rohan-gupta-3b478b1a0)
