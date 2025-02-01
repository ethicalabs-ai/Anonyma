# Anonyma  

Anonyma will be a multilingual text anonymization tool designed to identify and mask sensitive information in textual data.

It will leverage transformer-based models to replace personally identifiable information (PII) with anonymized placeholders, ensuring privacy without compromising text usability. The project focuses on custom fine-tuning using LoRA (Low-Rank Adaptation) for efficiency and performance.

---

## Planned Features

- **Multilingual Support:** Process text in multiple languages.
- **Entity Recognition:** Detect and anonymize entities such as names, dates, and locations.
- **Customizable:** Allow users to define which entities to anonymize.

---

## Possible Models

To effectively handle both entity recognition and text transformation, Sequence-to-Sequence (Seq2Seq) transformer models are recommended:

1. **T5 (Text-to-Text Transfer Transformer)**  
   - **Description:** A flexible model that can handle various NLP tasks by framing them as text-to-text problems. Suitable for multilingual anonymization with fine-tuning.  
2. **mBART (Multilingual BART)**  
   - **Description:** A multilingual variant of BART, designed for tasks involving multiple languages. Ideal for anonymizing text across diverse languages.
3. **Non-Instruction Transformer SLMs (Qwen2.5, Phi-Series)**  
   - **Description:** Encoder-decoder Small Language Models optimized for NLP tasks without instruction tuning. These models provide consistent task-focused outputs without misinterpreting prompts.

---

## Possible Datasets

To train and evaluate Anonyma, the following datasets from Hugging Face can be used:

1. **PII Masking 200k**  
   - **Description:** Contains over 200,000 examples for training models to mask PII in English, French, German, and Italian.  
   - [PII Masking 200k Dataset](https://huggingface.co/datasets/ai4privacy/pii-masking-200k)

2. **PII Masking 300k**  
   - **Description:** An expanded version with 300,000 examples across multiple languages.  
   - [PII Masking 300k Dataset](https://huggingface.co/datasets/ai4privacy/pii-masking-300k)
