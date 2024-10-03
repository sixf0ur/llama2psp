## llama2psp

A quick homebrew for running [llama2.c](https://github.com/karpathy/llama2.c) on the PSP.

![image](./IMG0.jpeg)

## Prerequisites

You will need docker and can use the [ticky/pspdev](https://hub.docker.com/r/ticky/pspdev/) docker image.

```shell
docker pull ticky/pspdev
```

## How to build
- Clone this repo and `cd` into the repo folder.

Run:
```shell
docker run -it --rm -v "$PWD:/src" ticky/pspdev make
```

## Installation
- Put the `EBOOT.PBP` in the following directory `PSP/GAME/llama2psp/EBOOT.PBP` as well as the model named `model.bin` and tokenizer named `tok.bin`
- Models and tokenizer have to be in the llama2.c format and can be downloaded [here](https://huggingface.co/karpathy/tinyllamas/tree/main)

- Due to the hardware limitations of the PSP, I used the smallest [260k model](https://huggingface.co/karpathy/tinyllamas/resolve/main/stories260K/stories260K.bin?download=true) and its [tokenizer](https://huggingface.co/karpathy/tinyllamas/resolve/main/stories260K/tok512.bin?download=true).
