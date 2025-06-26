# Fermat Near Miss Finder

## Program Details

* **File Name:** `fermat_near_miss.py`
* **External Files Required:** None
* **External Files Created:** None
* **Programmers:** Keba Paul
* **Email Address:** kebapaul@lewisu.edu
* **Course Number and Section:** SU25-CPSC-60500-001
* **Date Submitted:** 2025-06-15

## Description

This program searches for "near misses" to Fermat’s Last Theorem. Given an exponent `n` (with 2 < `n` < 12) and an upper bound `k` (>10) for base integers `x` and `y`, it iterates over all combinations of `x` and `y` from 10 to `k`. For each pair, it computes `x^n + y^n` and identifies the integer `z` such that `z^n` is the closest to `x^n + y^n`.

The program reports the smallest relative miss found, printing out each time a new smallest relative miss is discovered, and summarizing the final smallest miss at the end.

## Resources Used

* Python documentation on integer math and power functions
* https://realpython.com/python-int-sequence/#finding-the-closest-integer

## How to Run the Program (Python Script )

To run this program directly from the Python script, follow these steps:

1. **Ensure Python is installed:** You need Python 3.x installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
2. **Save the file:** Save the provided Python code as `fermat_near_miss.py` in a directory of your choice.
3. **Open a terminal or command prompt:** Navigate to the directory where you saved the file.
4. **Run the script:** Execute the following command:
   ```bash
   python fermat_near_miss.py
   ```
5. **Follow the prompts:** The program will ask you to enter the exponent `n` and the maximum value for `x` and `y`.

## Building the Executable

To create a standalone executable (`.exe` for Windows, or equivalent for other OS) that can be run without installing Python, we will use `PyInstaller`.

### Prerequisites

* Python 3.x installed.
* `pip` (Python package installer) installed (usually comes with Python).

### Steps to Build the Executable

1. **Install PyInstaller:** Open your terminal or command prompt and install `PyInstaller` using pip:

   ```bash
   pip install pyinstaller
   ```
2. **Navigate to the script directory:** Change your current directory in the terminal to where `fermat_near_miss.py` is saved.

   ```bash
   cd /path/to/your/script/
   ```

   (Replace `/path/to/your/script/` with the actual path to your file.)
3. **Build the executable:** Run the following command. The `--onefile` option bundles everything into a single executable file.

   ```bash
   pyinstaller --onefile fermat_near_miss.py
   ```

   This process might take a few moments. You will see output indicating the progress.
4. **Locate the executable:**

   * After successful execution, `PyInstaller` will create a `dist` folder in the same directory.
   * Inside the `dist` folder, you will find the executable file (e.g., `fermat_near_miss.exe` on Windows, or `fermat_near_miss` on Linux/macOS).
   * You can run this executable directly.
