🕊️ SolaceVR LLM
SolaceVR LLM is an experimental domain-specific large language model project focused on spiritually grounded text, particularly from the Latter-day Saint tradition. While the initial goal was to build a bespoke LLM from scratch using foundational texts like the Book of Mormon, Doctrine and Covenants, and Joseph Smith Translation, we encountered critical feasibility barriers. This repo captures our progress, methods, and lessons learned from the project.

📚 Project Vision
SolaceVR aimed to create a spiritually aware AI agent capable of interacting with users in a VR setting, providing faith-informed responses rooted in canonical Latter-day Saint scriptures. The long-term vision was a model that could:

Answer theological questions from LDS sources

Engage in scriptural conversation in immersive VR

Understand nuances in different versions of LDS texts

🧠 Dataset
We curated a specialized dataset totaling ~4.5 million words drawn from:

The Book of Mormon (multiple editions)

Doctrine and Covenants

Pearl of Great Price

King James Bible + Joseph Smith Translation

Seminary manuals and topical study guides

These were compiled and cleaned into a text corpus used for tokenization and exploratory model training.

🏗️ Model Approach
We initially attempted to prototype a language model using Hugging Face’s transformers library and tokenized data from the curated scriptures. Some of the major steps:

Tokenization using AutoTokenizer with a custom vocabulary

Experiments with nanoGPT for a smaller character-level model

⚠️ Challenges
Despite efforts, we hit key roadblocks:

Insufficient data volume: ~150M tokens is not enough to train a competitive model from scratch.

Model hallucination: Without a robust retrieval system or larger base model, early outputs lacked scriptural precision.

Compute limitations: Training larger models was prohibitively expensive or slow even with cloud GPUs.

✅ What Worked
Creating a clean, semantically grouped LDS corpus

Embedding scripture references and commentary into prompts

Testing retrieval-augmented generation (RAG) setups with chunked verses and seminary notes

🔄 Future Direction
Although full LLM training from scratch isn't practical, the project seeded ideas for:

Fine-tuning pre-trained models (e.g. Mistral, LLaMA) with LDS doctrine via LoRA

Embedding-based scripture retrieval bots

Audio/chat-based VR spiritual guides powered by lightweight models
