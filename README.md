# PDF to Image Converter

A professional, client-side PDF to image conversion tool built with vanilla JavaScript. Convert PDF documents to high-quality images with advanced features including automatic whitespace removal and long-form image merging.

## Features

### Core Functionality
- **Client-side Processing**: All conversions happen in your browser - no server uploads required
- **Multiple Output Formats**: Support for PNG (high quality) and JPEG (compressed) formats
- **Quality Control**: Adjustable resolution scaling from 1x to 3x
- **Batch Processing**: Handle multi-page PDFs efficiently

### Advanced Features
- **Dual Conversion Modes**:
  - Separate Mode: Convert each PDF page to individual images
  - Long-form Mode: Merge all pages into a single continuous image
- **Intelligent Whitespace Removal**: Automatically detect and trim empty margins
- **Customizable Spacing**: Control spacing between pages in long-form mode
- **Batch Download**: ZIP packaging for multiple images or direct download for merged images

### User Experience
- **Drag & Drop Interface**: Intuitive file upload with visual feedback
- **Real-time Progress**: Live conversion progress with detailed status updates
- **Responsive Design**: Optimized for desktop and mobile devices
- **Error Handling**: Comprehensive error reporting and validation

## Technical Specifications

### Dependencies
- **PDF.js**: Mozilla's PDF rendering library for client-side PDF processing
- **JSZip**: JavaScript library for creating ZIP archives
- **Canvas API**: HTML5 canvas for image rendering and manipulation

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### File Limitations
- Maximum file size: 50MB
- Supported format: PDF only
- No password-protected PDFs

## Installation

### Quick Start
1. Download the HTML file
2. Open in any modern web browser
3. No additional setup required

### Local Development
```bash
# Clone or download the project
git clone [your-repository-url]

# Open the HTML file in your browser
open pdf-to-image-converter.html
```

### Web Deployment
The application is a single HTML file with embedded CSS and JavaScript. Deploy to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Amazon S3
- Any web server

## Usage Guide

### Basic Conversion
1. Select conversion mode (Separate or Long-form)
2. Choose output format and quality settings
3. Upload PDF file via drag-and-drop or file picker
4. Wait for conversion to complete
5. Download individual images or complete ZIP archive

### Conversion Modes

#### Separate Mode
Converts each PDF page to an individual image file. Ideal for:
- Document archival
- Individual page extraction
- Standard PDF to image conversion

#### Long-form Mode
Merges all PDF pages into a single continuous image. Features include:
- Automatic whitespace detection and removal
- Configurable page spacing
- Intelligent content alignment
- Perfect for continuous documents, comics, or presentations

### Whitespace Removal Options
- **Auto Detection**: Remove whitespace from all sides
- **Top Only**: Remove only header whitespace
- **Bottom Only**: Remove only footer whitespace
- **None**: Preserve original page dimensions

## API Reference

### Configuration Options

#### Image Format
```javascript
formatSelect.value = 'png' | 'jpeg'
```

#### Quality Settings
```javascript
qualitySelect.value = '1' | '1.5' | '2' | '3'
```

#### Conversion Mode
```javascript
modeSelect.value = 'separate' | 'merge'
```

#### Whitespace Trimming
```javascript
trimSelect.value = 'auto' | 'top' | 'bottom' | 'none'
```

### Core Functions

#### PDF Processing
```javascript
convertPDFToImages(file)          // Main conversion function
convertToSeparateImages(pdf)      // Separate mode processing
convertToLongImage(pdf)           // Long-form mode processing
```

#### Image Manipulation
```javascript
trimWhitespace(canvas, mode)      // Remove whitespace from canvas
mergeCanvases(canvases, spacing)  // Combine multiple canvases
```

## Performance Considerations

### Memory Usage
- Large PDFs may consume significant browser memory
- Recommended maximum: 100 pages for optimal performance
- High-quality settings increase memory requirements

### Processing Time
Conversion time depends on:
- PDF page count
- Selected quality setting
- Document complexity
- Device performance

### Optimization Tips
- Use JPEG format for faster processing and smaller files
- Lower quality settings for quicker conversion
- Close other browser tabs during large file processing

## Security & Privacy

### Data Protection
- No data transmission to external servers
- All processing occurs within your browser
- Files are not stored or cached
- Complete privacy and security

### Browser Limitations
- Subject to browser memory limits
- No access to system files outside of selected documents
- Automatic cleanup of temporary data

## Troubleshooting

### Common Issues

#### Large File Errors
- **Cause**: File exceeds 50MB limit or browser memory
- **Solution**: Use smaller files or reduce quality settings

#### Conversion Failures
- **Cause**: Corrupted PDF or unsupported features
- **Solution**: Try a different PDF or check file integrity

#### Performance Issues
- **Cause**: Insufficient device memory or processing power
- **Solution**: Close other applications, use lower quality settings

#### Browser Compatibility
- **Cause**: Outdated browser version
- **Solution**: Update to latest browser version

### Error Messages
- "Please select a PDF file": Wrong file type selected
- "File size cannot exceed 50MB": File too large
- "PDF conversion failed": Processing error occurred

## Contributing

### Development Setup
1. Fork the repository
2. Make changes to the HTML file
3. Test in multiple browsers
4. Submit pull request with detailed description

### Code Style
- Use consistent indentation (2 spaces)
- Comment complex functions
- Follow existing naming conventions
- Test across different PDF types

### Feature Requests
Submit issues with:
- Clear feature description
- Use case explanation
- Expected behavior
- Current limitations

## License

MIT License

Copyright (c) 2024 PDF to Image Converter
Created by: clarezhangstr@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Contact

For questions, suggestions, or support, please contact:
- Email: clarezhangstr@gmail.com
- Issues: Please use the GitHub Issues page for bug reports and feature requests

## Acknowledgments

- Mozilla PDF.js team for the excellent PDF rendering library
- JSZip contributors for reliable ZIP archive functionality
- Browser vendors for robust Canvas API implementations

## Version History

### v1.0.0
- Initial release with basic PDF to image conversion
- Support for PNG and JPEG formats
- Quality control and batch processing

### v1.1.0
- Added long-form conversion mode
- Implemented intelligent whitespace removal
- Enhanced user interface and progress reporting
- Improved error handling and validation

### v1.2.0
- Optimized memory usage for large files
- Added configurable page spacing
- Enhanced mobile device compatibility
- Improved conversion speed and reliability


### v1.3.0

- Shadcn/UI Design System Integration: Complete visual overhaul using Shadcn/UI components
- Dark/Light Theme Support: Full theme switching with automatic system preference detection
- Internationalization: Complete Chinese and English language support with dynamic switching
- Modern UI Components: Card layouts, improved buttons, and professional form controls
- Enhanced Accessibility: Better keyboard navigation and screen reader support
- Responsive Design Improvements: Optimized mobile experience with adaptive layouts
- Theme Persistence: Intelligent theme and language preference storage with fallback support
- Visual Polish: Smooth transitions, consistent spacing, and professional color schemes

