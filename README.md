# Financial Spreadsheet Agent Pipeline

A Jupyter Notebook workflow for analyzing Excel spreadsheets through a LangGraph state-based agent. The workflow accepts a natural-language question, selects an analysis tool, validates generated queries, and returns spreadsheet results.

## What it demonstrates

- State-based orchestration with LangGraph `StateGraph`
- LLM-assisted query generation and validation
- Spreadsheet loading and preview with Pandas
- DataFrame operations for straightforward analysis
- DuckDB SQL queries for more complex operations
- Query-result validation, error handling, and bounded iteration
- Handling of missing values and numeric edge cases in query validation

## Tools in the workflow

- `load_preview_data` — inspects spreadsheet columns, data types, and sample rows
- `simple_dataframe_query` — evaluates Pandas-based operations in a restricted environment
- `complex_duckdb_query` — runs SQL against a registered Pandas DataFrame

## Prerequisites

- JupyterLab, Google Colab, or another notebook environment
- Python packages used by the notebook: `langchain`, `langgraph`, `pandas`, `python-dotenv`, and `duckdb`
- An LLM API key configured for the model used by the notebook

## Run the notebook

1. Clone the repository:

   ```bash
   git clone https://github.com/tejaswi-6189/fin-sheet-agent-pipeline.git
   cd fin-sheet-agent-pipeline
   ```

2. Open `ExcelWorkerLLMToolCallAgent.ipynb` in JupyterLab or Google Colab.

3. Configure the required LLM environment variables in the notebook environment.

4. Run the notebook cells in order. The first setup cell installs the required Python libraries.

5. Provide an Excel file in the notebook's working directory and ask a question about its data.

## Notebook

- [`ExcelWorkerLLMToolCallAgent.ipynb`](ExcelWorkerLLMToolCallAgent.ipynb)
