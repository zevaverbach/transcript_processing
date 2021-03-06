# tpro

Transcript Processing! `tpro` takes transcripts produced by
various speech-to-text services and converts them to various standardized
formats.

![demo](demo.gif)

# Installation and Usage

## Non-pip Requirement:  Stanford NER JAR

  - download and unzip [this](https://nlp.stanford.edu/software/stanford-ner-2018-10-16.zip)
  - put these files in in /usr/local/bin/:
    - stanford-ner.jar
    - classifiers/english.all.3class.distsim.crf.ser.gz
  - you might have to [update Java](https://askubuntu.com/questions/508546/howto-upgrade-java-on-ubuntu-14-04-lts) on Linux

## Pip

    $ pip install tpro

## Usage

    $ tpro --help

    Usage: tpro [OPTIONS] TRANSCRIPT_DATA_PATH OUTPUT_PATH
                [amazon|gentle|speechmatics|google] [universal|vo]

    Options:
      -p, --print-output    pretty print the transcript, breaks pipeability
      --language-code TEXT  specify language, defaults to en-US.
      --help                Show this message and exit.

# STT Services

- [Speechmatics](https://www.speechmatics.com/)
- [Amazon Transcribe](https://aws.amazon.com/transcribe/)
- [Gentle](https://github.com/lowerquality/gentle)
- [Google Cloud Speech-to-Text](https://cloud.google.com/speech-to-text/)

## Planned

- [Watson](https://www.ibm.com/watson/services/speech-to-text/) 
- [Mozilla's new open-source STT thing](https://github.com/mozilla/DeepSpeech)

# Output Formats

- [Universal Transcript](https://gist.github.com/zevaverbach/d2b7a19397607677878aa3268fda1002#example) (JSON)
- [viraloverlay](https://github.com/zevaverbach/viraloverlay#json-transcript-format) (JSON)

## Planned

- Draft.js JSON
- Word (`.doc`, `.docx`)
- text files
- SRT (subtitles)
