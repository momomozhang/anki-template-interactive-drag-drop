# Anki Interactive Drag-Drop Template

This repository contains an interactive flashcard template for Anki, featuring drag-and-drop functionality with comprehensive visual feedback and game-like features.

![image](https://github.com/user-attachments/assets/e220cf30-e9e1-40a4-b8c3-557a27999f5c)

![image](https://github.com/user-attachments/assets/d458ad52-5f54-4a5c-aade-818c0a2e25b9)

## Key Features

### Interactive Learning Experience
- **Intuitive Drag-and-Drop**: Simply drag terms into the correct categories with visual guidance
- **Smart Randomization**: Every review shuffles both terms and categories to ensure true learning
- **Instant Feedback**: Get immediate +1 or -1 scores with helpful hints for wrong answers
- **Flexible Organization**: Sort your remaining terms alphabetically or keep them random

### Enhanced Study Features  
- **Multiple Answer Support**: Some terms can belong to multiple categories - just separate with |
- **Adaptive Layouts**: Choose horizontal layout for fewer categories or vertical for many categories
- **Complete Solutions**: Flip the card to see all correct answers organized properly
- **Reset and Retry**: Made mistakes? Reset and try again without losing progress

### Customizable Content
- **Scalable Categories**: Create exercises with 2-9 different categories
- **Rich Visual Design**: Duolingo-inspired interface with smooth animations
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices

### Learning Benefits
- **Prevents Memorization**: Random ordering stops you from memorizing positions
- **Active Recall**: Drag-and-drop engages motor memory alongside visual learning
- **Immediate Correction**: See mistakes instantly with hints to the correct category
- **Progress Tracking**: Clear visual indicators show your performance


## Layout Options

### Horizontal Layout ("H")
- **Structure**: Headers appear as columns across the top row
- **Appearance**: Wide table format
- **Use case**: Good when you have fewer categories or when category names are short
- **Example**:
  ```
  | Animals | Colors | Countries |
  |---------|--------|-----------|
  | [drop]  | [drop] | [drop]    |
  ```

### Vertical Layout ("V")
- **Structure**: Headers appear as rows down the left side
- **Appearance**: Tall, narrow table format
- **Use case**: Better when you have many categories or when category names are long
- **Example**:
  ```
  |           | Terms  |
  |-----------|--------|
  | Animals   | [drop] |
  | Colors    | [drop] |
  | Countries | [drop] |
  ```

## Files
- `front.html`: The HTML code for the front side of the flashcard with complete JavaScript logic.
- `back.html`: The HTML code for the back side of the flashcard (shows front side).
- `style.css`: The CSS styling for the interactive interface.
- `Example.apkg`: Example Anki deck file for testing and demonstration.
  

## Setup Guide

### Prerequisites
- Anki Desktop application installed
- Basic familiarity with Anki's note type management

### Step 1: Create the Note Type
1. Open Anki Desktop
2. Go to **Tools** → **Manage Note Types**
3. Click **Add** to create a new note type
4. Choose **Add: Basic** and name it "Interactive Drag-Drop"
5. Click **Fields...** to manage the fields

### Step 2: Add Required Fields
You need to create exactly **21 fields** with these exact names (case-sensitive):

**Core Fields:**
- `Title` - The main exercise title

**Category Fields:**
- `Header1`, `Header2`, `Header3`, `Header4`, `Header5`, `Header6`, `Header7`, `Header8`, `Header9`

**Term Fields:**
- `Terms1`, `Terms2`, `Terms3`, `Terms4`, `Terms5`, `Terms6`, `Terms7`, `Terms8`, `Terms9`

### Step 3: Configure Templates
1. Click **Cards...** to edit the card templates
2. **Front Template**: Delete all existing content and paste the entire contents of `front.html`
3. **Back Template**: Delete all existing content and paste the entire contents of `back.html`
4. **Styling**: Delete all existing content and paste the entire contents of `style.css`

### Step 4: Test the Setup
1. Import the provided `Example.apkg` file to see a working example
2. Create a test card with your note type
3. Fill in the `Title`, at least 2 `Header` fields, corresponding `Terms` fields, and set `Layout` to "H" or "V"
4. Use the `|` character to separate multiple correct answers within terms (e.g., `cat|feline|kitty`)

### Step 5: Creating Cards
- **Flexible Categories**: You can use anywhere from 2-9 categories - just leave unused Header/Terms fields blank
- **Multiple Answers**: Separate alternative answers with `|` (pipe character)
- **Layout Choice**: Use "H" for fewer categories (2-4), "V" for more categories (5-9)


## License
[MIT License.]
