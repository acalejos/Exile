# Exile

[![Twitter Follow](https://img.shields.io/twitter/follow/ac_alejos?style=social)](https://twitter.com/ac_alejos)

A small [Livebook](https://livebook.dev/) file to automatically censor explicit audio using AI.

This will use OpenAI's whisper model to both transcribe and timestamp words. Then a separate local model trained
on offensive content will be used to identify words to beep.

The model is fairly high on false positives when used on single words, so you might want to implement a confidence
threshold or better yet just include a list of words to beep if it would be fairly short and exhaustive.

You will also need to make sure you have the `ffmpeg` binary installed in `PATH` and visible to the Livebook
environment.
