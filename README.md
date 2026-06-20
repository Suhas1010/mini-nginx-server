# Mini Static File Server

A lightweight static file server built from scratch using Node.js core modules without relying on any external frameworks such as Express.

This project demonstrates the fundamental working principles of a web server, including request handling, file serving, MIME type detection, and error handling.

---

## Features

* Serves static files such as HTML, CSS, JavaScript, and images.
* Handles incoming HTTP requests.
* Dynamically maps URLs to corresponding files.
* Supports MIME type detection for different file extensions.
* Returns custom `404 File Not Found` responses for missing resources.
* Built entirely using Node.js core modules without any third-party dependencies.

---

## Tech Stack

* Node.js
* HTTP Module
* File System (`fs`) Module
* Path Module

---

## Project Structure

```text
project-folder/
│
├── server.js          # Main server file
├── index.html         # Homepage
├── style.css          # Stylesheet
├── script.js          # Client-side JavaScript
├── images/            # Static assets (optional)
└── README.md
```

---

## How It Works

1. The server listens for incoming requests on port `3000`.
2. When a client requests a resource, the server extracts the requested URL.
3. The URL is mapped to a file path on the local file system.
4. The server determines the appropriate MIME type based on the file extension.
5. The requested file is read using the File System module.
6. If the file exists:

   * The server responds with status code `200 OK`.
   * The file content is sent back to the browser.
7. If the file does not exist:

   * The server responds with status code `404 Not Found`.

---

## Supported MIME Types

| Extension | MIME Type         |
| --------- | ----------------- |
| `.html`   | `text/html`       |
| `.css`    | `text/css`        |
| `.js`     | `text/javascript` |
| `.png`    | `image/png`       |

---

## Installation and Usage

### Clone the repository

```bash
git clone <repository-url>
```

### Navigate to the project directory

```bash
cd <project-folder>
```

### Run the server

```bash
node server.js
```

### Open your browser and visit

```text
http://localhost:3000
```

---

## Example Request Flow

```text
Browser Request
       ↓
HTTP Server Receives Request
       ↓
Extract URL (req.url)
       ↓
Map URL to File Path
       ↓
Determine MIME Type
       ↓
Read File from Disk
       ↓
File Exists?
    /        \
  Yes        No
   ↓          ↓
Send 200    Send 404
Response    Response
```

---

## Learning Outcomes

Through this project, I gained practical understanding of:

* HTTP request-response lifecycle
* Static file serving
* URL routing fundamentals
* MIME types and response headers
* File handling using Node.js
* HTTP status codes
* Core backend concepts without frameworks

---

## Future Improvements

* Add support for additional file types.
* Implement custom error pages.
* Add request logging.
* Introduce caching mechanisms.
* Add support for directory-based routing.
* Extend the project into a full backend server using Express.

---

## Author

**Suhas**

Built as part of my backend learning journey to understand how web servers work under the hood.
