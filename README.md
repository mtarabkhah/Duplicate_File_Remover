# Duplicate File Remover

The Duplicate File Remover is a Python script that helps you find and manage duplicate files in a given set of directories. It allows you to identify duplicate files, calculate their sizes, generate a report, and optionally move or delete the duplicate files.

## Features

- Search for duplicate files in multiple directories.
- Support for various file extensions, including images (JPG, JPEG, PNG) and videos (MP4, MOV, AVI).
- Calculate the total size of unique files and duplicated versions.
- Generate an Excel report with detailed information about original files and their duplicates.
- Option to move duplicate files to a specified destination folder.
- Option to delete duplicate files (permanently or move to the recycle bin/trash).

## Requirements

- Python 3.x
- `PIL` library (for image processing)
- `openpyxl` library (for generating Excel reports)
- `send2trash` library (for sending files to the recycle bin/trash)

## Usage

1. Clone or download the code from the repository.
2. Install the required packages by running `pip install -r requirements.txt` in your terminal.
3. Update the `directories` and `extensions` variables in the code to specify the directories you want to search for duplicates and the file extensions to consider.
4. Run the script:
   ```shell
   python duplicate_file_remover.py
   ```
5. The script will display the total number and size of files, as well as the number and size of unique files and duplicated versions.
6. An Excel report named `duplicate_files_report.xlsx` will be generated, containing two sheets: "Original Files" and "Duplicated Files."
7. If you want to move or delete the duplicate files, provide the `destination_folder` or modify the `delete_flag` variable in the code.
8. In case of deleting the files, there are 2 options of deleting permanently or moving into Recycle Bin/Trash, which can be selected by modifying the `delete_permanently` variable in the code.
9. Re-run the script to perform the selected action (move or delete).
10. The first file of the duplicated files has been selected as the main file to keep. This can be modified by updating `main_file_index = 0` as required.

Note: This is an educational version and might have issues or bugs. Please use caution when deleting or moving files. It's recommended to review the generated report and double-check the selected files before performing any irreversible actions.

## Limitations

- The duplicate detection algorithm relies on file hashing (MD5) and image metadata (EXIF) to identify duplicates. It may not detect all cases, especially if the rotated versions are stored differently in the files.
- The script uses the `send2trash` library to send files to the recycle bin/trash. The behavior may vary depending on the operating system and configuration.
- Detecting rotated versions of images as duplicates has been commented out as it is not working properly.
- For more accurate duplicate detection, advanced image comparison techniques or deep learning-based methods can be explored.

## Future Works

- Adding a GUI to the code.
- Converting from .py to .exe.
- Detecting rotated versions of images as duplicates.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to create a pull request or submit an issue.