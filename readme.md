# Password Generator

This project is a web-based **Password Generator** application built with HTML, CSS, and JavaScript. The generator allows users to create strong and random passwords with customizable options such as password length, inclusion of uppercase/lowercase letters, numbers, and symbols. Users can copy the generated password to their clipboard or download it as a text file.

## Table of Contents
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Customization](#customization)

---

## Features

1. **Password Length Customization**: Choose the length of the password (between 4 and 20 characters).
2. **Character Set Customization**: Include or exclude the following:
   - Uppercase letters
   - Lowercase letters
   - Numbers
   - Symbols
3. **Clipboard Copy**: Copy the generated password to the clipboard with a single click.
4. **Password Download**: Download the generated password as a `.txt` file.
5. **Responsive Design**: Adaptable to different screen sizes for both mobile and desktop users.

## Demo

You can try the live demo of the password generator [here](https://hungry-goodall-5f8dc5.netlify.app/).

---

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/anshitmishraa/password-generator.git
    ```

2. Navigate to the project directory:
    ```bash
    cd password-generator
    ```

3. Open `index.html` in your browser to view the application locally.

---

## Usage

1. Open the Password Generator app.
2. Customize the password options:
   - Adjust the length using the number input.
   - Check/uncheck options to include/exclude uppercase, lowercase letters, numbers, and symbols.
3. Click the **Generate Password** button.
4. The generated password will be displayed in the result box.
5. Use the **Clipboard** button to copy the password or click **Download** to save the password as a text file.

### Example

1. Select:
   - Length: 12
   - Include Uppercase: Yes
   - Include Lowercase: Yes
   - Include Numbers: Yes
   - Include Symbols: Yes
2. Click "Generate Password".
3. Example generated password: `Ax8!op$W7q@2`
4. Copy the password to the clipboard or download it.

---

## Code Structure

```
password-generator/
│
├── css/
│   └── styles.css           # Styling for the password generator
│
├── js/
│   └── main.js              # JavaScript logic for password generation, clipboard copy, and file download
│
├── index.html               # Main HTML structure
├── README.md                # Documentation
```

### Key Files:
- **index.html**: The structure of the application (headings, inputs, buttons).
- **css/styles.css**: Contains the styles for UI, such as button styles and layout.
- **js/main.js**: The core logic of the password generator:
  - Password creation based on user preferences.
  - Copying the password to the clipboard.
  - Downloading the password as a `.txt` file.

### Detailed Explanation of the Core Functions

1. **`generatePassword(lower, upper, number, symbol, length)`**: 
   - Generates a random password based on the selected options.
   - Iterates over the user-selected options (lowercase, uppercase, etc.) and constructs the password by randomly picking characters from each category.
   - Returns the final password trimmed to the desired length.

2. **Clipboard Copy**: 
   - The password is copied to the clipboard using `document.execCommand('copy')`.
   - An alert is shown to confirm successful copy.

3. **Download as File**:
   - The `saveAs` method from the `FileSaver.js` library is used to download the password as a `.txt` file.

---

## Customization

To modify the password generation logic:

1. **Change Character Sets**:
   - You can customize the character sets for uppercase, lowercase, numbers, or symbols in the `getRandomLower`, `getRandomUpper`, `getRandomNumber`, and `getRandomSymbol` functions in the `js/main.js` file.

2. **Extend Password Length**:
   - By default, the password length is limited to between 4 and 20 characters. This can be modified by updating the `min` and `max` attributes in the password length input field:
     ```html
     <input type="number" id="length" min="4" max="50" value="20" />
     ```

3. **Styling**:
   - Modify the `css/styles.css` file to change the appearance of the generator. You can alter the button colors, font sizes, and layout as per your preference.
