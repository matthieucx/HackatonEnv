## Setup

1. Install VSCode (in programs folder)
2. Install extension (5th icon, 4 squares) by copy-pasting the following IDs in search bar:
    - ms-python.python
    - ms-toolsai.jupyter
    - mechatroner.rainbow-csv
    - tomoki1207.pdf
    - GrapeCity.gc-excelviewer
3. Install Git (in programs folder)
4. Clone this repository (3rd icon in VSCode left sidebar)
5. Open a terminal. This is found in ribbon at the top, or in the three dots in the ribbon. Terminal > New Terminal
6. Install Python project manager tool: `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/0.4.16/install.ps1 | iex"`
7. Create your programming environment: `uv sync`.

Do you need to do certificate stuff ?

### What if I have some of these tools already?

No issue! Use what you like. I still recommend using uv, it manages Python installation, virtual environments, and dependencies for you. This will ensure that you have the same environment as everyone else.

## Accelerators provided

- [ARGUS](https://github.com/Azure-Samples/ARGUS): An app that extracts information from documents, and gives you structured data. Can be constrained to a specific user-defined schema.
- document_comparer (created by the Microsoft Coaches): A notebook showcasing how to compare changes between two documents with GenAI.
- Buildcopilotwith-cache-and-your-data (created by the Microsoft Coaches): A RAG app using your data, leveraging a cache of answers to avoid unnecessary searches.
- [chat-with-your-data-solution-accelerator](https://github.com/Azure-Samples/chat-with-your-data-solution-accelerator):
- [azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo)

## Running code

### Azure ressources

Accelerators are dependent on specific Azure ressources. Necessary information to connect to them are passed to the applications as environment variables, defined in a .env file. Those are present in the different folders of the accelerators.

If you have permissions or connection issues, those variables may be incorrect. Please ask your coach and/or Frantz, our Cloud Engineer.

### Launch projects

In the terminal, type: `uv run <path_to_file>`. For example, `uv run src/hello.py`. This is equivalent to running `python src/hello.py`, but ensures your environment is always correct. 

If you want to use a Jupyter notebook, open it in VSCode. In the top right of the file, click Select Kernel and choose `.venv (Python 3.11.9) .venv\Scripts\python.exe`.

### ARGUS

This accelerators uses ressources deployed in Azure Cloud. A web application that connects to those ressources is launched using a tool called Streamlit. To launch it: `uv run streamlit accelerators/ARGUS/frontend/app.py`.