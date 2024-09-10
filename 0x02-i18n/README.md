# Flask i18n & Localization Project

This project implements internationalization (i18n) and localization (l10n) for a Flask web application using Flask-Babel. The aim is to create a multilingual app that adapts based on user language preferences and time zones.

## Project Overview

The key objectives of this project include:
- **Parametrizing Flask templates** to display content in multiple languages (English and French).
- **Inferring the correct locale** based on URL parameters, user settings, or request headers.
- **Localizing timestamps** to display times based on the user’s time zone.

### Features
1. **Basic Flask App**: Set up a simple Flask application to serve localized content.
2. **Locale Detection**: Use URL parameters, request headers, or user settings to determine the user's preferred language.
3. **Template Localization**: Translate dynamic content using Flask-Babel and Jinja2 templates.
4. **User-Specific Settings**: Simulate user login to display personalized messages and locale-specific content.
5. **Time Zone Handling**: Infer and display the correct time based on the user’s time zone.

### Requirements
- Python 3.7
- Flask 1.1.2
- Flask-Babel 2.0.0
- pytz for timezone handling
- Ubuntu 18.04 LTS

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/major0001/alx-backend.git
   cd alx-backend/0x02-i18n
   ```

2. Install the required packages:
   ```bash
   pip3 install -r requirements.txt
   ```

3. Run the Flask app:
   ```bash
   python3 0-app.py
   ```

4. Access the app at `http://127.0.0.1:5000/`.

### Translation Setup

To set up translations, follow these steps:
1. Extract message IDs:
   ```bash
   pybabel extract -F babel.cfg -o messages.pot .
   ```

2. Initialize translations for supported languages:
   ```bash
   pybabel init -i messages.pot -d translations -l en
   pybabel init -i messages.pot -d translations -l fr
   ```

3. Compile the translations:
   ```bash
   pybabel compile -d translations
   ```

### File Structure
```bash
0x02-i18n/
├── templates/
│   ├── 0-index.html
│   ├── 1-index.html
│   └── ... # Other template files
├── translations/
│   ├── en/
│   ├── fr/
├── 0-app.py
├── 1-app.py
├── ...
├── babel.cfg
└── README.md
```
