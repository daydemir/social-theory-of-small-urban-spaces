# Selection-Based Word Count Setup

This document explains the word count configuration for Markdown (.md) and LaTeX (.tex) files.

## What Has Been Configured

### 1. VS Code (Fully Working)
The **Selection Word Count** extension by witulski has been installed and is ready to use:
- Extension ID: `witulski.selection-word-count`
- When you select text in Markdown files, the status bar will show the word count of the SELECTED text
- When no text is selected, it shows the total document word count
- No additional configuration needed - it works automatically

### 2. LaTeX Files (.tex)
LaTeX Workshop has been configured to show word count:
- Setting: `"latex-workshop.texcount.autorun": "onSave"`
- Word count appears in status bar after saving the file
- Requires the `texcount` utility to be installed on your system

Configuration added to:
- `/Users/deniz/Build/mit/social/.vscode/settings.json` (workspace settings)
- `/Users/deniz/Library/Application Support/Cursor/User/settings.json` (global settings)

### 3. Cursor IDE (Partial Support)
Cursor has limited extension marketplace access. The Selection Word Count extension is not available in Cursor's marketplace.

## How to Use in VS Code

1. Open any Markdown (.md) file
2. Select some text
3. Look at the status bar (bottom of window)
4. You'll see: "Words: X" where X is the count of selected words

## Options for Cursor IDE

Since Cursor doesn't have the Selection Word Count extension available, you have these options:

### Option A: Use VS Code for Editing (Recommended)
When you need selection-based word counts, edit in VS Code where the extension is already installed and working.

### Option B: Manual VSIX Installation (Advanced)
1. Download the VSIX file from one of these sources:
   - VS Code: Extensions view → Right-click "Selection Word Count" → Download VSIX
   - VsixHub: https://www.vsixhub.com/vsix/41212/

2. Install in Cursor using one of these methods:
   - Command Palette: `Extensions: Install from VSIX...`
   - Command line: `cursor --install-extension /path/to/selection-word-count.vsix`
   - Drag & drop the .vsix file into Cursor's Extensions panel

### Option C: Alternative Extension
Try installing a different word count extension that might be available in Cursor's marketplace:
- Search for "word count" or "markdown" in Cursor's Extensions view
- Look for extensions that support selection counting

## Verification

### In VS Code:
1. Open this file (WORD_COUNT_SETUP.md)
2. Select this sentence
3. Check the status bar - you should see a word count

### For LaTeX:
1. Open a .tex file
2. Make some edits
3. Save the file (Cmd+S)
4. Check status bar for word count (requires texcount utility)

## Technical Details

### Configuration Files Modified:
1. `/Users/deniz/Build/mit/social/.vscode/settings.json` (created)
2. `/Users/deniz/Library/Application Support/Cursor/User/settings.json` (updated)

### Extensions Installed:
- VS Code: `witulski.selection-word-count@0.0.2` ✓

## Troubleshooting

### LaTeX word count not showing:
Install texcount utility:
```bash
# Using Homebrew
brew install texcount

# Or if you have TeX Live installed, it should already be included
```

### Selection count not working in VS Code:
1. Check extension is enabled: View → Extensions → Search "Selection Word Count"
2. Reload window: Cmd+Shift+P → "Developer: Reload Window"
3. Check for markdown file type: Status bar should show "Markdown"

## References
- [Selection Word Count Extension](https://marketplace.visualstudio.com/items?itemName=witulski.selection-word-count)
- [LaTeX Workshop Features](https://github.com/James-Yu/latex-workshop/wiki/ExtraFeatures)
- [Cursor VSIX Installation Guide](https://forum.cursor.com/t/how-to-install-vsix-format-extension/1667)
