# PI AF Hierarchy Generator

**PI AF HIERARCHY GENERATOR**  
**POWERED BY MATANGI INFOTECH**

A browser-based Excel utility that reads a raw workbook's headers, lets the user choose and reorder hierarchy columns, and exports a PI AF Element list.

## Features
- Reads .xlsx, .xls and .xlsm files in the browser using SheetJS.
- Detects worksheet headers and suggests likely hierarchy columns.
- Lets users include/exclude and reorder any detected column.
- Supports variable hierarchy depth and branching.
- Creates each unique parent/child Element path once.
- Exports exactly: Selected(x), Parent, Name, ObjectType.
- Does not create Attributes.

## GitHub Pages
The app is in `/pi-af-hierarchy-generator/`. If GitHub Pages is enabled for this repository with the `main` branch and root folder, open:

https://mann2324.github.io/pi-af-hierarchy-generator/

## Use
1. Upload a source Excel workbook.
2. Select the worksheet.
3. Review detected headers; tick hierarchy columns only.
4. Move columns up/down to set parent-to-child order.
5. Set the root parent path (default: DFPCL).
6. Generate preview and download the Excel file.

## Data handling
Workbook parsing and generation happen in the user's browser. The workbook is not uploaded to a backend. SheetJS is loaded from jsDelivr, so an internet connection is needed to load the library.

## Important
Review the preview before importing into PI AF. Confirm the root path and column order match the target AF database. This tool generates Element rows only; it does not create Attributes or configure PI Point Data References.
