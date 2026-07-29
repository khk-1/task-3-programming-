# Voice Assistant Project

## Project Overview
This project is a PHP-based Voice Assistant that communicates with the Google Gemini API to generate responses from user input.

---

# Project Setup

The following steps were performed to upload and run the project:

1. Downloaded the project files.
2. Copied the project folder into the XAMPP `htdocs` directory.
3. Started Apache from the XAMPP Control Panel.
4. Opened the project using:
   ```
   http://localhost/voice-assistant/
   ```
5. Configured the Gemini API key inside `config.php`.
6. Tested the application and verified that it was communicating successfully with the Gemini API.

---

# Problems Found

## Problem 1: Incorrect Home Page

### Issue
The main page was named `index-2.html`, so Apache displayed the directory listing instead of loading the application.

### Solution
Renamed the file:

```
index-2.html
```

to

```
index.html
```

---

## Problem 2: Incorrect Backend Path

### Issue
The JavaScript file was sending requests to:

```
api/chat.php
```

while the actual backend file was:

```
ro.php
```

### Solution
Updated the backend URL inside `app.js` to point to the correct PHP file.

---

## Problem 3: Incorrect PHP Configuration Path

### Issue
The PHP backend attempted to load:

```php
require __DIR__ . '/../config.php';
```

Although `config.php` was located in the same directory.

### Solution
Changed it to:

```php
require __DIR__ . '/config.php';
```

---

## Problem 4: Missing API Key

### Issue
The Gemini API key was not configured.

### Solution
Generated a Gemini API key from Google AI Studio and added it to:

```php
config.php
```

---

## Problem 5: Unsupported Gemini Model

### Issue
The project used an old Gemini model that is no longer available for new users.

The API returned an error indicating that the model had been deprecated.

### Solution
Updated the project to use a currently supported Gemini model, allowing successful communication with the API.

---

# Final Result

After applying all fixes:

- The project loads correctly.
- PHP backend works successfully.
- Gemini API responds correctly.
- Voice assistant functions as expected.

---

# Screenshot
results.png


