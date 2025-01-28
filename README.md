# Word Replacement Script

This script is designed to replace all occurrences of a specified word in the files located within a directory tree. The script is written in Python.

## Usage

This script is used from the command line with three arguments:

1. The word you want to replace (`word_old`).
2. The new word you want to use (`word_new`).
3. The root file or directory path.

**Here is an example usage**:
```bash
python3 word_replacement.py oldWord newWord /path/to/your/directory
```

## Functionality

The script starts by taking three command-line arguments: the old word, the new word, and the root directory/file path.

The script then defines a helper function findall(text, word) to find all occurrences of a word in a given text.

Next, the script uses the os.walk() function to iterate over all files in the directory tree rooted at the provided file path. For each file, it attempts to read its contents and find all occurrences of the old word.

If the old word is found in a file, the script replaces it with the new word, and then writes the new content back to the file.

If any errors occur while reading or writing a file, the script will simply ignore them and continue to the next file.
Caution

Please use this script with caution. It directly modifies the files under the specified directory. It is recommended to back up your files before running this script.
