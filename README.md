# llmchat

The project is being developed by the following Sekcja Sztucznej Inteligencji members: Eldar Aliekpierov, Natalia Błaszczyk, Maciej Cichoń, Agata Świetlik.  

# Project description

The solution is aimed towards helping TUL staff and aspiring students navigate the university's documentation. The user can ask the bot a question related to some document from the TUL database (e.g. "How many terms are there to pass an exam?") and the bot will respond with accurate, up-to-date information on the topic (e.g. "Students have 3 tries at passing an exam..."). Something more relevant for future TUL students is the "course recommendation system", with it being one of the features of the bot. A high school graduate (maturzysta) can send the bot their exam grades, subject preferences along with other information that could help determine the best-fit course for the individual, and the bot will respond with its recommendation based on the provided information.

Сurrently houses a minimal implementation of RAG, along with the beginings of not-so-minimal one.
Different base models are being tested on [TruthfulQA](https://github.com/sylinrl/TruthfulQA), with different embedding models being tested on [LEPISZCZE](https://arxiv.org/abs/2211.13112) and [KLEJ](https://arxiv.org/abs/2005.00630)
The project is still under heavy development, implying possible functionality, UI or any other kinds of changes.

# Usage

docker run -p 6333:6333 -v ~/path/to/loca/vector/database:/qdrant/storage:z qdrant/qdrant

ollama create newmodelname --file path/to/model/file

uvicorn app:app --reload
