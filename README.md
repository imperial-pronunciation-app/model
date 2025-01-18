# Model

## Methodology

We are fine-tuning Whisper for audio to phonemes transcription trained using the TIMIT dataset.

As we want the model to output phonemes instead of text, we need to construct a custom tokeniser. We can reuse the pre-trained feature extractor. We take the pre-trained tiny.en model, freezing the encoder layers and fine-tuning the decoder layers, changing the output layer dimension for phonemes.
