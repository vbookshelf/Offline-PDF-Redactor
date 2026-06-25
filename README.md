# Offline PDF Redactor
A minimalist browser based single-file PDF redactor that audits its own ouput.

Live demo:



<br>

Drawing a black box over text does not hide it. It just places a vector shape on top of the text layer. This leaves the underlying text completely extractable via a simple copy-paste or Ctrl + F search.

This app  applies true destructive flattening (Rasterization). Instead of just overlaying a black rectangle annotation over a PDF text object, this app destroys the original document structure:

- Renders the PDF page directly into raw canvas pixels.

- Burns the black boxes straight into that pixel buffer.

- Exports the final page as a compressed flat image layer inside a new PDF.

Because the output is just a picture of the redacted page, there is no underlying text metadata to exploit.

<br>

## Self Verification

The app programmatically audits its own output right after generation. It immediately re-parses the redacted file with pdf.js to ensure the character count is exactly zero. In other words, it performs a Ctrl + F search to ensure that no text is extractable.

## How to use ofline
Simply download the project folder and place it on your desktop. Then double click the index.html file. The app will open in your browser.

## How to manually verify that redacted text has been burned out



<br>

## Revision History

Version 1.0<br>
27-June-2026<br>
First release.

<br>



