# Copilot Instructions for JSE Sector Momentum Project

## Project Overview
This project focuses on analyzing sector momentum in the Johannesburg Stock Exchange (JSE). The primary goal is to collect, process, and visualize financial data to identify trends and insights.

### Key Components
- **Data Collection**: The `01_data_collection.ipynb` notebook is the entry point for collecting financial data using the `yfinance` library.
- **Environment Setup**: A Python virtual environment is used for dependency management. Ensure the virtual environment is activated before running any scripts.

## Developer Workflows

### Setting Up the Environment
1. Ensure Python is installed on your system.
2. Activate the virtual environment:
   ```powershell
   .\venv\Scripts\Activate.ps1
   ```
3. Install required dependencies:
   ```powershell
   pip install -r requirements.txt
   ```

### Running the Notebook
1. Open `01_data_collection.ipynb` in VS Code.
2. Ensure the virtual environment kernel is selected.
3. Execute cells sequentially to collect and process data.

### Debugging
- Use `print` statements to debug issues in the notebook.
- Check library versions to ensure compatibility:
  ```python
  print(f"pandas version: {pd.__version__}")
  print(f"yfinance version: {yf.__version__}")
  ```

## Project-Specific Conventions
- **Notebook Structure**: Each notebook cell should have a clear purpose, such as importing libraries, data collection, or visualization.
- **Error Handling**: Use try-except blocks to handle API errors when fetching data with `yfinance`.
- **Version Logging**: Log library versions at the start of the notebook to ensure reproducibility.

## External Dependencies
- **yfinance**: Used for fetching financial data.
- **pandas**: For data manipulation.
- **matplotlib**: For data visualization.

## Integration Points
- The project relies on `yfinance` for external data. Ensure API calls are within rate limits.

## Example Patterns
### Importing Libraries
```python
import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt
```

### Fetching Data
```python
data = yf.download("AAPL", start="2020-01-01", end="2020-12-31")
```

### Visualizing Data
```python
plt.plot(data['Close'])
plt.title("Closing Prices")
plt.show()
```

## Key Files
- `01_data_collection.ipynb`: Main notebook for data collection and analysis.
- `venv/`: Virtual environment for dependency management.

---

For any issues or questions, refer to the `README.md` (if available) or consult the project owner.