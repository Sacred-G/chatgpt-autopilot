# ChatGPT-AutoPilot

A ChatGPT API powered Python script that can build almost anything with the power of the [Function Calling] 

(https://openai.com/blog/function-calling-and-other-api-updates). 

Just tell it what you want to build, and it will build it and ask you clarifying questions along the way.


# Usage


```
$ ./gpt-autopilot.py
```

## Linux

You can either clone the repository and run `gpt-autopilot.py` 

1\. Export your [OpenAI API key](https://platform.openai.com/account/api-keys) as `OPENAI_API_KEY` environment variable or put it in the `config.json` file (see `config.sample.json`). You can also run the program directly, and it will ask you for your API key.

```console
$ export OPENAI_API_KEY=YOUR_API_KEY
```

2\. Install the **latest** version of the `openai` python package
```console
$ pip install --upgrade openai
```

3\. Run the script. It will ask you for a prompt.

```console
$ ./gpt-autopilot.py
```

## Where does the output go?

The files will be written to the `code` directory, relative to the path of the executable. If you use the `--dir` flag, files will be written to the directory you specify. If you use the `--versions` flag, the files will be written to the `versions` directory.

## Does it work with GPT-3.5 or GPT-4?

Yes. The default model is `gpt-3.5-turbo-16k-0613`. You can change it in the `config.json` file. Make sure to use the 0613 models since only they support function calling. GPT-4 (`gpt-4-0613`) will provide more capabilities for certain tasks, but will be a lot more expensive. It is recommended to try it with GPT-3.5 first.

## ATTN

If you are getting an error with the OpenAI api. If your on windows and cant upgrade try uninstalling openai and reinstalling using pip install openai===0.28.0. If your running linux you will probabaly get a prompt to update via 
the command line.



