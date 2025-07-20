# WP Flask Post Generator (v0.2)

This is a standalone Flask application designed to generate and publish posts to WordPress. This version (0.2) is distributed as a single executable file, ensuring ease of use without requiring Python or library installations on the target system. Sensitive information like API keys, passwords, and site links are not hardcoded or stored within the distributed executable or its initial database.

## Table of Contents
1.  [Features](#features)
2.  [Getting Started](#getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Running the Application](#running-the-application)
3.  [Initial Setup and Configuration](#initial-setup-and-configuration)
4.  [Application Usage](#application-usage)
    *   [Dashboard](#dashboard)
    *   [Topics](#topics)
    *   [Posts](#posts)
    *   [Settings](#settings)
5.  [Troubleshooting](#troubleshooting)

## 1. Features
*   Generate post content using Gemini API.
*   Publish generated content to WordPress.
*   Manage topics for post generation.
*   Configure WordPress and Gemini API settings via a web interface.

## 2. Getting Started

### Prerequisites
*   **Operating System**: Windows (The executable is built for Windows 64-bit).
*   **Internet Connection**: Required for interacting with Gemini API and WordPress.

### Running the Application
1.  **Locate the Executable**: Navigate to the `dist` folder within the project directory. You will find `WP_Flask_v0.2.exe`.
2.  **Delete Existing Database (Optional but Recommended for Clean Start)**: If you have previously run the application and wish to start with a fresh database, delete the `database.db` file from the main project directory (e.g., `f:\Ai Projects\Ai WP Flask\database.db`).
3.  **Run the Executable**: Double-click `WP_Flask_v0.2.exe` or open a command prompt/terminal in the `dist` directory and run:
    ```bash
    .\WP_Flask_v0.2.exe
    ```
    A console window will appear, indicating that the Flask server is running. Do not close this window while using the application.

## 3. Initial Setup and Configuration
Upon first running the application (or after deleting `database.db`), the application will automatically create a new, empty `database.db` file.

1.  **Access the Application**: Open your web browser and go to `http://127.0.0.1:5000/`.
2.  **Settings Page Redirection**: The application will automatically redirect you to the `/settings` page if essential settings (WordPress URL) are not yet configured.
3.  **Enter Your Credentials**: On the settings page, you must provide the following information:
    *   **Gemini API Key**: Your API key for the Google Gemini API.
    *   **WordPress URL**: The base URL of your WordPress site (e.g., `https://your-wordpress-site.com`).
    *   **WordPress Username**: Your WordPress username with publishing permissions.
    *   **WordPress Password**: Your WordPress application password (not your regular user password). If you don't have one, generate it in your WordPress dashboard under Users -> Your Profile -> Application Passwords.
    *   **Default Post Status**: (Optional) Choose a default status for new posts (e.g., "draft", "publish").
4.  **Save Settings**: Click the "Save Settings" button. Once saved, the application will be ready for use.

## 4. Application Usage

### Dashboard
The main dashboard provides an overview of your application.

### Topics
Manage topics for your posts. You can add new topics and update their status.

### Posts
Generate and publish new posts. You can specify prompts, length, tone, audience, SEO keywords, outline, and language for content generation.

### Settings
Modify your Gemini API and WordPress credentials, or other application settings.

## 5. Troubleshooting
*   **"no such table: settings" error**: This indicates the database was not initialized correctly. Ensure you deleted any old `database.db` file and then re-ran the executable. The application should create a fresh database automatically.
*   **Application not accessible**: Ensure the console window for `WP_Flask_v0.2.exe` is still open and running. Check if the port 5000 is free on your system.
*   **WordPress API issues**: Double-check your WordPress URL, username, and especially the application password in the `/settings` page. Ensure your WordPress site is accessible and the REST API is enabled.
*   **Gemini API issues**: Verify your Gemini API key in the `/settings` page. Ensure you have an active internet connection.