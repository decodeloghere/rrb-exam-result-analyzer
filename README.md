# RRB Exam Result Analyzer

A lightweight Chrome extension that automatically analyzes RRB exam response sheets and displays a detailed result summary, including correct answers, incorrect answers, unattempted questions, and wrong question serial numbers.

Built to help Railway Recruitment Board (RRB) exam candidates review their response sheets quickly without manually checking every question.

## Features

- **Total Questions** – Displays the total number of questions in the response sheet.
- **Attempted Questions** – Counts questions where an option was selected.
- **Correct Answers** – Calculates the number of correctly answered questions.
- **Incorrect Answers** – Calculates the number of incorrectly answered questions.
- **Unattempted Questions** – Shows how many questions were left unanswered.
- **Wrong Question Numbers** – Lists the serial numbers of incorrectly answered questions.
- **Side-by-Side Summary** – Displays the result panel alongside the response sheet.
- **Console Statistics** – Prints a structured result summary in Chrome Developer Tools.
- **Lightweight** – Uses native JavaScript without external libraries or dependencies.

## Supported Exams

The extension is intended for RRB examination response sheets that use compatible question and answer HTML structures.

It can be useful for candidates appearing in examinations such as:

- RRB ALP – Assistant Loco Pilot
- RRB Technician
- RRB NTPC
- RRB Group D
- RRB JE – Junior Engineer
- Other RRB examinations with compatible response-sheet structures

**Compatibility note:** Not every RRB examination or response-sheet version uses the same HTML structure. Compatibility depends on the question, selected-option, and correct-answer elements used by the response-sheet page.

## How It Works

The extension reads the response-sheet content directly from the browser and compares the selected option against the correct answer.

For each question:

1. Detects the selected option.
2. Reads the correct answer.
3. Compares both options.
4. Updates the correct or incorrect count.
5. Records the serial number of incorrect questions.

Questions without a selected option are counted as unattempted.

The extension then creates a summary panel beside the response-sheet table.

## Installation

### Method 1: Install from Source

1. Download or clone this repository.

   ```bash
   git clone https://github.com/decodeloghere/rrb-exam-result-analyzer.git
   ```

2. Open Google Chrome.

3. Navigate to:

   ```text
   chrome://extensions/
   ```

4. Enable **Developer mode**.

5. Click **Load unpacked**.

6. Select the downloaded extension folder.

7. Open your supported RRB response sheet or refresh the page.

The result summary will appear automatically when the response sheet contains the supported HTML structure.

### Method 2: Download ZIP

1. Open this repository on GitHub.
2. Click **Code → Download ZIP**.
3. Extract the downloaded ZIP file.
4. Open `chrome://extensions/`.
5. Enable Developer mode.
6. Click **Load unpacked** and select the extracted folder.

## Project Structure

```text
rrb-exam-result-analyzer/
│
├── manifest.json
├── content.min.js
├── main.min.js
└── README.md
```

| File | Description |
|---|---|
| `manifest.json` | Chrome extension configuration |
| `content.min.js` | Exam response-sheet analysis and result panel |
| `main.min.js` | Prevent Built-in page timer to reload page |

## Privacy

Your privacy matters.

- No account registration is required.
- No external API is used.
- No response-sheet data is uploaded to a server.
- No personal information is intentionally collected.
- Analysis is performed locally in your browser.

The extension reads the response-sheet content available on the page to calculate the result.

## Important Disclaimer

This is an independent, community-developed utility.

- This project is **not affiliated with, endorsed by, or officially associated with Railway Recruitment Board (RRB), Indian Railways, or any government organization**.
- The calculated results depend on the correctness and availability of the response-sheet data.
- This tool is intended for personal analysis and educational purposes.
- Always refer to the official RRB response sheet and official examination updates for authoritative information.

## Contributing

Contributions are welcome!

If the extension does not work with a particular RRB examination or response-sheet format, you can help improve compatibility.

1. Fork this repository.
2. Create a new branch.
3. Make your changes.
4. Test the extension with the relevant response-sheet format.
5. Submit a Pull Request.

Please avoid sharing personal candidate information, registration numbers, roll numbers, or other sensitive examination details in public issues.

## Report an Issue

If you encounter a problem:

1. Open the repository's **Issues** section.
2. Describe the RRB examination and response-sheet format.
3. Explain what is not working.
4. Share a sanitized HTML sample if necessary.

Never upload a response sheet containing personal candidate information.

## License

Choose and add an open-source license before publishing this repository. The license determines how others may use, modify, and distribute your code.
