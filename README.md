# Image Captioning Virtual Assistant using Deep Learning

## Project Overview
This project demonstrates a deep learning-based virtual assistant that can automatically generate descriptive captions for images and convert them into spoken output using text-to-speech (TTS). It mimics how humans perceive and describe visual content, enabling accessibility tools, content automation, and smart assistants.

## Business Problem
With the explosion of visual data across digital platforms, there's a growing need for systems that can understand and describe images intelligently—especially for visually impaired users, content creators, and automated tagging systems. This project aims to bridge that gap by generating context-aware image captions and making them audible, enabling smarter user experiences.

## Tools & Technologies
* TensorFlow, Keras – for deep learning model development
* InceptionV3 – as CNN-based image feature extractor
* Custom Encoder-Decoder model with Bahdanau Attention
* NLTK – for BLEU score evaluation
* gTTS – Google Text-to-Speech for voice conversion
* Matplotlib, PIL – for image & attention visualization

## Methodology

1. Data Preprocessing: Cleaned and tokenised captions, padded sequences, and extracted image features using InceptionV3.
2. Model Architecture: Implemented a CNN-RNN hybrid architecture:
   * Encoder: CNN to extract visual features
   * Decoder: LSTM with Attention to generate text
3. Training Strategy: Used teacher forcing and masked loss for stable training. BLEU score used for evaluation.
4. Caption Evaluation:Visualised attention maps over image regions and evaluated accuracy using BLEU scores.
5. Virtual Assistant Feature: Converted predicted captions to speech using gTTS, enabling the assistant to "speak" its descriptions.

## Key Results
* Achieved BLEU scores up to 52.2 on test images.
* Accurately generated context-specific captions like:
> Real: "white dog with black collar jumps up to catch tennis ball"\
> Predicted: "white dog is leaping into the air to catch ball"
* Deployed attention visualisations to highlight which parts of the image the model focused on while generating each word.

## Use Cases
* Assisting visually impaired users through verbal image descriptions
* Automated caption generation for social media, e-commerce, and surveillance
* Smart assistant features that "see and speak"

## Conclusion
This project proves the feasibility of combining computer vision, natural language processing, and speech synthesis to build an end-to-end image-to-audio captioning assistant. It demonstrates how deep learning can create accessible, intelligent systems capable of understanding and communicating visual content—paving the way for enhanced human-AI interaction.
