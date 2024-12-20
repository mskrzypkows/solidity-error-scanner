# Solidity Error Code Scanner

A CLI tool that scans Solidity files for error declarations and generates their corresponding 4-byte error codes.

## Installation

1. Clone this repository
2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Linux/Mac
# or
.\venv\Scripts\activate  # On Windows
```
3. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the script by providing the directory to scan:

```bash
python scanner.py /path/to/solidity/files
```

The tool will:
1. Recursively scan all `.sol` files in the specified directory
2. Find error declarations (e.g., `error INSUFFICIENT_MINT_FEE();`)
3. Generate and print the 4-byte error codes for each error found

## Example Output

```
In file: /path/to/file.sol
Error: INSUFFICIENT_MINT_FEE
Code: 0x2c5211c6
```