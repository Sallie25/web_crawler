# Site Map Generator

## Description
Site Map Generator is a command-line tool designed to crawl a given domain URL, gather all internal links, and output a tree structure representation of the website. It also generates XML or HTML sitemap files to assist with SEO and general site analysis.

## Key Features

### Domain Crawling
- **Recursive Crawling**: Start from a root URL (e.g., `https://example.com`) and recursively visit all pages within the domain.
- **Crawl Depth Limiting**: Configure crawl depth to prevent excessive or infinite crawling.
- **Error Handling**: Gracefully handle broken links, redirects, and avoid repeated visits to the same pages.
- **Ignore External Links**: Focus on internal links only.

### Site Map Generation
- **XML Sitemap**: Generate a sitemap in XML format for search engines.
- **HTML Sitemap**: Optionally create a user-friendly HTML version of the sitemap showing the website hierarchy.
- **File Saving**: Save generated sitemaps locally, with optional upload support to a specified location.

### Tree Output
- **Website Hierarchy**: Represent the website structure as a tree in either a console output or a saved file (e.g., JSON or plain text).

### Command-Line Interface (CLI)
- **Single Command Execution**: Run the tool using commands like:
  ```bash
  python site-map-generator.py --url "https://example.com" --depth 3
  ```
- **Configurable Parameters**: Adjust depth, output folder, and file formats through CLI arguments.

### Error Handling & Logging
- **Comprehensive Logs**: Capture HTTP errors, redirects, and unreachable links.
- **Verbose Messages**: Provide clear logs for troubleshooting crawling issues.

### Extensibility
- **Modular Design**: Easily integrate additional features or connect the tool to larger systems.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Sallie25/site-map-generator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd site-map-generator
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the generator with a single command:
```bash
python site-map-generator.py --url "https://example.com" --depth 3 --output ./sitemaps
```

### CLI Parameters
- `--url`: The root URL to start crawling (required).
- `--depth`: Limit the depth of the crawl (default: unlimited).
- `--output`: Specify the folder to save generated files (default: current directory).
- `--format`: Specify output format(s), such as `xml`, `html`, or `json` (default: `xml`).

### Example
To crawl `https://example.com`, limit depth to 2, and save the results in the `output` folder:
```bash
python site-map-generator.py --url "https://example.com" --depth 2 --output ./output --format xml html
```

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Added new feature"
   ```
4. Push the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.





