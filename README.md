# HW4 Project – Caprese

## Introduction
Today, we can see services that turn speech into text almost everywhere. For example, the dictate feature in phones and smart TVs. That being said, it is often a struggle to get the device to type what you are saying as it may misinterpret the words as something else. This is why, in this notebook, we decided to test out Google Cloud's Speech to Text machine learning API to see how well it would do when transcribing speech.

## Google Cloud's Speech to Text
Google Cloud's machine learning API Speech to Text allows you to convert speech into text using Google’s AI technologies. Speech to Text can transcribe content in real time or from stored files, deliver an improved user experience through voice commands, and improve service based on customer interactions.

Benefits of this API include state-of-the-art accuracy, global reach, and flexible deployment. Google’s most advanced deep learning neural network algorithms enable automatic speech recognition (ASR). Voice recognition supports over 125 different languages, and speech recognition can be deployed in the cloud or on premises.

Key features, such as speech adaptation, allow you to customize speech recognition to transcribe domain-specific terms and rare words. You can also automatically convert spoken numbers into addresses, years, and currencies using classes.

You are able to choose from different domain-specific models for voice control, phone call, and video transcription, which are optimized for domain-specific quality requirements.

Streaming speech recognition provides real-time speech recognition results as the API processes the audio input streamed from your application’s microphone.

And lastly, Speech-to-Text On-Prem can be deployed in your own private data centers to ensure full conrtol and protection.

## How It Works

![](https://raw.githubusercontent.com/carolinelee78/HW4_Caprese/main/DrawIo.png)
Our process involves downloading sample recordings of speech in varying languages from omniglot and storing them in cloud storage. Then, using the Google Speech to Text API we run the audio files to get the text output. These results were then stored in BigQuery and confidence intervals were created to assess the accuracy of the Speech to Text API for each language.

## Data Visualizations 
Check out the data visualizations in [Data Studio](https://datastudio.google.com/reporting/10d771f4-7eb0-46f8-abe8-d485dc8c9ab4)

## Conclusions 
We conducted tests using Google’s Speech-to-Text API for three different phrases and in 5 different languages. We gave the API phrases in Korean, Slovenian, Vietnamese, Icelandic, and Persian. There was a range of accuracy from the different languages as well as the different phrases. For “Thanks”, the confidence level ranged from 60.1% with Slovenian to 97.6% with Icelandic. For “How are you?”, the confidence levels ranged from 83.4% in Vietnamese to 96.1% confidence in Icelandic. The phrase “Happy Birthday” was interesting as well, because we saw Korean fall off in confidence a lot compared to the other two phrases, reaching only 74.6% confidence, while Slovenian shot all the way up to 95.8% confidence. Icelandic remained solid in the third phrase though, at 97.6%, demonstrating that Google’s Speech-to-Text API is quite good at discriminating the translation of phrases in Icelandic compared to the other languages.
