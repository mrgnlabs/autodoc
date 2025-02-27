[View code on GitHub](https://github.com/context-labs/autodoc/src/cli/commands/index/prompts.ts)

The code in this file provides three functions that generate prompts for documentation experts to create summaries and answer questions about code files and folders in a project. These functions are likely used in the larger autodoc project to automate the process of generating documentation for code files and folders.

1. `createCodeFileSummary`: This function takes five parameters: `filePath`, `projectName`, `fileContents`, `contentType`, and `filePrompt`. It returns a formatted string prompt for a documentation expert to write a summary of the code file. The prompt includes the file path, project name, content type, and a custom file prompt. For example:

```javascript
createCodeFileSummary('src/example.js', 'autodoc', 'console.log("Hello, World!");', 'JavaScript', 'Write a detailed technical explanation of what this code does.');
```

2. `createCodeQuestions`: This function takes five parameters: `filePath`, `projectName`, `fileContents`, `contentType`, and `targetAudience`. It returns a formatted string prompt for a documentation expert to generate three questions and answers that a target audience might have about the code file. The prompt includes the file path, project name, content type, and target audience. For example:

```javascript
createCodeQuestions('src/example.js', 'autodoc', 'console.log("Hello, World!");', 'JavaScript', 'beginner');
```

3. `folderSummaryPrompt`: This function takes six parameters: `folderPath`, `projectName`, `files`, `folders`, `contentType`, and `folderPrompt`. It returns a formatted string prompt for a documentation expert to write a summary of the folder and its contents. The prompt includes the folder path, project name, content type, a list of files and their summaries, a list of subfolders and their summaries, and a custom folder prompt. For example:

```javascript
folderSummaryPrompt('src/', 'autodoc', [{fileName: 'example.js', summary: 'A simple example file'}], [{folderName: 'utils', summary: 'Utility functions'}], 'JavaScript', 'Write a detailed technical explanation of the folder structure and contents.');
```

These functions can be used in the autodoc project to generate prompts for documentation experts, helping to streamline the process of creating documentation for code files and folders.
## Questions: 
 1. **Question:** What is the purpose of the `createCodeFileSummary` function?
   **Answer:** The `createCodeFileSummary` function generates a string template for a code file summary prompt, which includes the file path, project name, file contents, content type, and a file prompt.

2. **Question:** How does the `createCodeQuestions` function differ from the `createCodeFileSummary` function?
   **Answer:** The `createCodeQuestions` function generates a string template for a code documentation prompt that asks for 3 questions and their answers, while the `createCodeFileSummary` function generates a string template for a code file summary prompt.

3. **Question:** What is the purpose of the `folderSummaryPrompt` function and what parameters does it take?
   **Answer:** The `folderSummaryPrompt` function generates a string template for a folder summary prompt, which includes the folder path, project name, files, folders, content type, and a folder prompt. It takes parameters such as folderPath, projectName, files, folders, contentType, and folderPrompt.