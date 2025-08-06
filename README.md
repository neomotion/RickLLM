# RickLLM

Welcome to **Rick-LLM**, a fine-tuned large language model that responds like the infamous genius scientist, **Rick Sanchez** from *Rick and Morty*. This project explores the customization of open-source LLMs through character-driven instruction tuning, curated dialogue datasets, tailored prompt engineering, and efficient deployment for local inference.


**Project Motivation**

The idea was to:

- Learn end-to-end fine-tuning of large language models (LLMs).

- Explore persona-based LLM customization.

- Use Rick Sanchez's dialogue style to simulate a unique, entertaining chatbot.

- Showcase local inference with GGUF quantization for edge-friendly deployments.


**Model Details**

- Base Model: Unsloth's Llama 3.2 3B

- Architecture: LLaMA 3.2-based instruction model

- Fine-Tuning Approach: QLoRA (Quantized Low-Rank Adapter)

- Quantization: GGUF (Q8_0 and Q4_0 available)

- Training Framework: Unsloth + Hugging Face + bitsandbytes


**Dataset Curation**

To replicate Rick’s unique voice:

- Gathered transcripts from Rick and Morty using open datasets & scripts.

- Cleaned data to remove other characters’ lines.

- Applied light data augmentation (paraphrased prompts).

- Split into instruction-tuning format ({"instruction", "input", "output"}).


**Training Configuration**

    model_name = 'unsloth/Llama-3.2-3B-Instruct',
    max_seq_length = 2048,
    dtype = None,  
    load_in_4bit = False,



**Results**

- The model convincingly mimics Rick’s tone — sarcastic, nihilistic, genius, drunk.

- Used prompt-based evaluation + human eval for qualitative judgment.
