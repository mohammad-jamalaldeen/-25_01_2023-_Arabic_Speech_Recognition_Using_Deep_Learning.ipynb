Whisper is a pre-trained model for automatic speech recognition (ASR) 
published in [September 2022](https://openai.com/blog/whisper/) by the authors 
Alec Radford et al. from OpenAI. Unlike many of its predecessors, such as 
[Wav2Vec 2.0](https://arxiv.org/abs/2006.11477), which are pre-trained 
on un-labelled audio data, Whisper is pre-trained on a vast quantity of 
audio-transcription data, 680,000 hours to be precise.

This is an order of magnitude more data than the un-labelled audio data used 
to train Wav2Vec 2.0 (60,000 hours). What is more, 117,000 hours of this 
pre-training data is multilingual ASR data. This results in checkpoints 
that can be applied to over 96 languages, many of which are considered 
_low-resource_.

When scaled to 680,000 hours of labelled pre-training data, Whisper models 
demonstrate a strong ability to generalise to many datasets and domains.
The pre-trained checkpoints achieve competitive results to state-of-the-art 
ASR systems, with a near 3% word error rate (WER) on the test-clean subset of 
LibriSpeech ASR and a new state-of-the-art on TED-LIUM with 4.7% WER ([Whisper paper]
(https://cdn.openai.com/papers/whisper.pdf)).

The extensive multilingual ASR knowledge acquired by Whisper during pre-training
can be leveraged for other low-resource languages; through fine-tuning, the pre-trained
checkpoints can be adapted for specific datasets and languages to further improve upon 
these results. I'll show just how Whisper can be fine-tuned for the Arabic language in this Colab.
