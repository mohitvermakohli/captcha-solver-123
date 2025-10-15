# CAPTCHA Entry Application

This is a simple, single-page web application designed to demonstrate a CAPTCHA entry mechanism. It displays an image from a specified URL or a default local file and allows the user to input the text they perceive from the image. The application then validates the user's input against a hardcoded expected value.

## Features

- **Dynamic Image Loading**: Loads CAPTCHA images via a URL query parameter (`?url=...`).
- **Default Image**: Falls back to a local `sample.png` if no URL is provided.
- **User Input Validation**: Compares user-entered text (case-insensitively) against a predefined CAPTCHA solution.
- **Responsive Design**: Built with Tailwind CSS for a modern, mobile-friendly interface.

## Getting Started

To run this application, you only need a web browser. Save the `index.html` file and ensure `sample.png` (the provided image with 'ADJRS') is in the same directory.

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, Safari, etc.)

### Installation

1.  Save the `index.html` content to a file named `index.html`.
2.  Place the `sample.png` image in the same directory as `index.html`.

## Usage

Open the `index.html` file directly in your web browser.

### Default Usage

If you open `index.html` without any query parameters, it will load the `sample.png` image. The expected CAPTCHA text for `sample.png` is `ADJRS`.

```
file:///path/to/your/project/index.html
```

### Custom Image URL

You can specify a custom image URL using the `url` query parameter. Replace `YOUR_IMAGE_URL_HERE` with the direct link to your CAPTCHA image.

```
file:///path/to/your/project/index.html?url=https://example.com/some-captcha-image.png
```

**Note**: For security reasons, browsers may block loading images from different origins (CORS policy) when accessed directly from a `file://` URL. For full functionality with external URLs, it is recommended to serve `index.html` via a local web server (e.g., `python -m http.server`).

### Solving the CAPTCHA

1.  Observe the image displayed.
2.  Type the characters you see into the input field.
3.  Click the "Submit CAPTCHA" button.
4.  The application will indicate whether your input matches the hardcoded expected value for the `sample.png` (or what it's configured to expect for other images if you modify the code).

## Development

This application uses:

-   **HTML5**: For structure.
-   **Tailwind CSS**: For utility-first styling (via CDN).
-   **Vanilla JavaScript**: For application logic.

No build tools or complex setup are required, making it easy to inspect and modify.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
