# Markdown Viewer

A clean and lightweight web-based markdown viewer with drag-and-drop file upload and instant PDF export.

## Features

- **Drag & Drop Upload** - Drop markdown files directly or use file picker
- **Full Markdown Support** - Renders all standard markdown syntax
- **PDF Export** - Convert viewed markdown to PDF with one click
- **Responsive Design** - Works seamlessly on desktop and mobile devices
- **Clean UI** - Professional interface with smooth interactions
- **No Installation** - Runs entirely in the browser, no setup required

## Quick Start

### Option 1: Open Directly
1. Download `index.html`
2. Double-click to open in your default browser
3. Start uploading markdown files

### Option 2: Local Server
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if you have http-server installed)
http-server
```
Then visit `http://localhost:8000` in your browser.

## Usage

1. **Upload a File**
   - Drag a `.md` or `.markdown` file into the upload area
   - Or click "Choose File" to select from your computer

2. **View Markdown**
   - Content renders instantly with proper formatting
   - File name displayed at the top
   - Supports headings, lists, tables, code blocks, and more

3. **Download as PDF**
   - Click "Download PDF" button (top right)
   - PDF saves with the original filename
   - Formatting matches the on-screen display

4. **Upload Another File**
   - Click "New File" to reset and upload a different markdown file

## Supported Markdown Syntax

- Headings (h1-h6)
- Paragraphs and line breaks
- Bold, italic, strikethrough
- Ordered and unordered lists
- Links and images
- Code blocks with syntax highlighting
- Inline code
- Blockquotes
- Tables
- Horizontal rules

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## File Structure

```
markdown-viewer/
├── index.html      # Complete application (HTML + CSS + JS)
└── README.md       # This file
```

## Technical Details

**Dependencies** (loaded via CDN):
- `marked.js` - Markdown parsing engine
- `html2pdf.js` - PDF generation library
- `html2canvas` - Canvas rendering for PDF export

**Technology Stack**:
- HTML5
- CSS3 with CSS Custom Properties
- Vanilla JavaScript (ES6+)
- No build tools or package managers required

## How It Works

1. Upload a markdown file
2. File is read and parsed by marked.js
3. HTML is rendered in the browser
4. When exporting to PDF:
   - Content is cloned to isolated container
   - html2canvas converts HTML to canvas
   - jsPDF converts canvas to PDF document
   - File downloads to your computer

## Limitations

- PDF export works best for documents under 50 pages
- Requires internet connection (uses CDN resources)
- Very large images may increase PDF file size
- Some advanced markdown extensions may not be supported

## Notes

- Single-file application for easy deployment and sharing
- All processing happens locally in your browser
- No data is uploaded to any server
- No cookies or local storage used
- Safe for private documents

## License

MIT License - Free to use, modify, and distribute

## Contributing

Found a bug or want to improve the tool? Contributions are welcome!

## Keyboard Shortcuts

- `Tab` - Navigate through buttons and upload area
- `Enter` - Click focused button
- `Space` - Activate button when focused

## Tips for Best Results

- Use standard markdown syntax for best compatibility
- Keep markdown files under 50 pages for optimal PDF quality
- Use relative image paths if including local images
- Test PDF export with a small file first

## Troubleshooting

**PDF is blank or empty:**
- Ensure markdown file is not too large
- Try with a simpler markdown file
- Check browser console for errors (F12)

**File won't upload:**
- Make sure file extension is `.md` or `.markdown`
- Try using the "Choose File" button instead of drag-drop
- Check file permissions

**Styling looks wrong:**
- Refresh the browser (Ctrl+F5 or Cmd+Shift+R)
- Try a different browser
- Clear browser cache

## Questions or Issues?

Check the markdown file format and try with a different file. If problems persist, check your browser's developer console for error messages.