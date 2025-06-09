# Based on Requirements

**Internet Connection:** A stable internet connection is crucial because the tool relies on an external web page for asset generation.
https://paperspleaseloc.github.io/

Download tool Papers-Please-Localization-Packer  

# Papers-Please-Localization-Packer
This tool automates the process of taking a translated text file (Loc.csv) for "Papers, Please" and generating all the necessary game assets (images with translated text, data files) required to use that translation in the game. It packages these assets into a .zip file, which is the format the game


**How to Use the Tool (Step-by-Step):**

1.  **Launch the Application:**
    *   Double-click on `Papers-Please Localization Packer.exe`.
    *   The main window titled "Papers, Please - Localization Packer" will appear.

2.  **Select the CSV File:**
    *   Click the "Browse" button next to the "CSV File:" field.
    *   A file dialog will open. Navigate to and select your prepared `Loc.csv` file.
    *   Click "Open". The path to your selected CSV file will now appear in the text box.

3.  **Enable Font Generation (Optional):**
    *   Look for the checkbox labeled "Enable Font Generation (--makeFonts)".
    *   **When to check this:** If your translation uses characters that are not well-supported by the game's default fonts (e.g., many non-Latin scripts, special symbols), or if your `Loc.csv` specifically requires custom fonts to be generated, check this box. The online tool it connects to will then attempt to generate appropriate font assets.
    *   If you are unsure, you can try running it without this option first. If text appears incorrectly in the game, try again with this option enabled.

4.  **Select the Output Directory:**
    *   Click the "Browse" button next to the "Output Dir:" field.
    *   A folder dialog will open. Navigate to and select the folder where you want the final localization pack (`.zip` file) to be saved. It's often a good idea to choose an empty folder or create a new one for this purpose.
    *   Click "Select Folder". The path to your chosen output directory will appear in the text box.

5.  **Start Packing:**
    *   Once you have selected the CSV file, decided on font generation, and chosen an output directory, click the "Start Packing" button.
    *   The button will become disabled (grayed out) while the process is running.

6.  **Monitor the Log:**
    *   The "Log:" text area at the bottom of the window will display progress messages, information about the files being processed, and any errors that might occur.
    *   This is where you'll see things like:
        *   `Starting process...`
        *   `Opening page: https://paperspleaseloc.github.io`
        *   `Loading csv from C:\path\to\your\Loc.csv`
        *   Messages about data files and images being processed (e.g., `[Image  1/123] assets/gfx/ImageName.png (WxH)`)
        *   `Zipping: C:\path\to\your\output\lang.zip` (where `lang` is the language code, like `en`, `de`, `jp`, etc., derived from your CSV).
        *   `Process finished.`

7.  **Retrieve Your Localization Pack:**
    *   When the process is complete, the "Log:" area will indicate "Process finished." and the "Start Packing" button will become enabled again.
    *   Navigate to the Output Directory you selected in Step 4.
    *   You should find a `.zip` file (e.g., `en.zip`, `fr.zip`). The name of the zip file (e.g., "en") is usually determined by the language code specified within the `Loc.csv` or how the underlying web tool interprets it.
    *   This `.zip` file is your localization pack, ready to be used with the game (you'll need to consult game-specific instructions or modding guides on how to install custom localization packs).
    *   **Temporary Folder:** The tool creates a temporary folder named `__tmp__<code>` (e.g., `__tmp__en`) inside your chosen output directory during processing. This folder contains all the individual generated files before they are zipped. After the `.zip` file is successfully created, you can usually delete this temporary folder.

**Troubleshooting/Important Notes:**

*   **Internet Connection:** A stable internet connection is crucial because the tool relies on an external web page for asset generation. If you have firewall or proxy issues, it might fail.
*   **Errors:** If any errors occur, they will be displayed in the "Log:" area. Copying these messages can be helpful if you need to seek help.
*   **Patience:** The process can take some time, especially if font generation is enabled or if there are many assets to process, as it involves browser automation, image manipulation, and file I/O.


This should cover how to use your `Papers-Please Localization Packer.exe`!
