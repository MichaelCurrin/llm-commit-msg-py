# About

## Project overview

The LLM Commit Msg project is a command-line tool that generates conventional commit messages by analyzing Git diffs using Large Language Models (LLMs).

The tool supports both local LLM servers (like Ollama) and cloud-based services (like OpenAI), providing users with intelligent, context-aware commit message generation while maintaining privacy and cost-effectiveness through local model options.

## Values

- Ease of use
- Security (using local LLM or self-hosted cloud LLMs are recommended over using subscription ChatGPT API)
- Quality of input

Speed is limited by what your local machine can do and what model can do, there is not much possible to improve on here.

## Requirements

- **Core functionality**: Generate conventional commit messages from Git diffs using LLM models
- **LLM integration**: Support multiple LLM providers including local servers (Ollama) and cloud services (OpenAI)
- **Git integration**: Read staged and unstaged changes, handle Git repository validation and error cases
- **Conventional commits**: Generate properly formatted commit messages following conventional commit specification
- **Cross-platform support**: Work on Linux and macOS
- **CLI interface**: Provide command-line interface with argument parsing and help documentation
- **Error handling**: Graceful handling of empty diffs, API failures, and Git repository errors
- **Configuration**: Environment-based configuration for API keys, hosts, and model names
- **Documentation**: Usage guides, installation instructions, and configuration documentation
- **Performance**: Handle large file changes efficiently with appropriate diff strategies


## What about running as an IDE extension?

If you prefer this LLM logic as an _extension_ in an IDE like VS Code instead of as a CLI, this tool has been rewritten as a VS Code extension:

- [MichaelCurrin/llm-commit-msg-vs-code](https://github.com/MichaelCurrin/llm-commit-msg-vs-code)

You can also search the extensions marketplace for extensions that generate commit messages. There are many there, but they tend to require a ChatGPT secret token and paid subscription and the extensions won't necessarily work with a local LLM or ChatGPT alternatives.

_Note: This CLI tool could also be written so there is an installable binary made with Go or as a Node app and then a VS Code extension to trigger that, but it's not worth the effort yet._
