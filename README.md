# File Protector

A Python script for batch encrypting PDF and Excel files while maintaining folder structure.

## Features

- Encrypts PDF and Excel (.xlsx, .xls) files with password protection
- Preserves original folder structure in the output
- Handles already encrypted PDFs with option to decrypt and re-encrypt
- Creates a new "Protected" folder with the original folder name
- Provides detailed operation summary and skipped files report

## Prerequisites

```bash
pip install PyPDF2
pip install msoffcrypto-tool
```

## Usage

```bash
python fileprotector.py <input_folder> <password>
```

Example:
```bash
python fileprotector.py "C:\Users\Documents\Reports" MySecurePassword123
```

This will:
1. Process all PDF and Excel files in the "Reports" folder and its subfolders
2. Create a new folder named "Protected Reports"
3. Save encrypted versions of all files in the new folder
4. Maintain the original subfolder structure

## Supported File Types

- PDF (.pdf)
- Excel (.xlsx, .xls)

## Error Handling

The script provides comprehensive error handling for:
- Already encrypted PDFs
- Invalid files
- Permission issues
- Missing folders

A summary is provided after completion showing:
- Successfully processed files
- Skipped files with reasons
- Total count of processed and skipped files

## License

[MIT License](LICENSE)
