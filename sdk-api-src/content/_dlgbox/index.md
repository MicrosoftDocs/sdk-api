---
UID: TP:dlgbox
ms.assetid: a28127d0-a8ac-381f-95fa-d472ee915ef7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Dialog Boxes



Overview of the Dialog Boxes technology.

To develop Dialog Boxes, you need these headers:

 * [commdlg.h](..\commdlg\index.md)

For the programming guide, see [Dialog Boxes](/windows/desktop/dlgbox).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CommDlgExtendedError function](..\commdlg\nf-commdlg-commdlgextendederror.md) | Returns a common dialog box error code. This code indicates the most recent error to occur during the execution of one of the common dialog box functions. |
| [FindTextA function](..\commdlg\nf-commdlg-findtexta.md) | Creates a system-defined modeless Find dialog box that lets the user specify a string to search for and options to use when searching for text in a document. |
| [FindTextW function](..\commdlg\nf-commdlg-findtextw.md) | Creates a system-defined modeless Find dialog box that lets the user specify a string to search for and options to use when searching for text in a document. |
| [GetCurrentDevMode function](..\commdlg\nf-commdlg-getcurrentdevmode.md) | Fills a DEVMODE structure with information about the currently selected printer for use with PrintDlgEx. |
| [GetCurrentPortName function](..\commdlg\nf-commdlg-getcurrentportname.md) | Retrieves the name of the current port for use with PrintDlgEx. |
| [GetCurrentPrinterName function](..\commdlg\nf-commdlg-getcurrentprintername.md) | Retrieves the name of the currently selected printer, for use with PrintDlgEx. |
| [GetFileTitleA function](..\commdlg\nf-commdlg-getfiletitlea.md) | Retrieves the name of the specified file. |
| [GetFileTitleW function](..\commdlg\nf-commdlg-getfiletitlew.md) | Retrieves the name of the specified file. |
| [GetOpenFileNameA function](..\commdlg\nf-commdlg-getopenfilenamea.md) | Creates an Open dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened. |
| [GetOpenFileNameW function](..\commdlg\nf-commdlg-getopenfilenamew.md) | Creates an Open dialog box that lets the user specify the drive, directory, and the name of a file or set of files to be opened. |
| [GetSaveFileNameA function](..\commdlg\nf-commdlg-getsavefilenamea.md) | Creates a Save dialog box that lets the user specify the drive, directory, and name of a file to save. |
| [GetSaveFileNameW function](..\commdlg\nf-commdlg-getsavefilenamew.md) | Creates a Save dialog box that lets the user specify the drive, directory, and name of a file to save. |
| [ReplaceTextA function](..\commdlg\nf-commdlg-replacetexta.md) | Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations. |
| [ReplaceTextW function](..\commdlg\nf-commdlg-replacetextw.md) | Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [LPCCHOOKPROC callback function](..\commdlg\nc-commdlg-lpcchookproc.md) | Receives messages or notifications intended for the default dialog box procedure of the Color dialog box. This is an application-defined or library-defined callback function that is used with the ChooseColor function. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_OFNOTIFYA structure](..\commdlg\ns-commdlg-_ofnotifya.md) | Contains information about a WM_NOTIFY message sent to an OFNHookProc hook procedure for an Open or Save As dialog box. The lParam parameter of the WM_NOTIFY message is a pointer to an OFNOTIFY structure. |
| [_OFNOTIFYEXA structure](..\commdlg\ns-commdlg-_ofnotifyexa.md) | Contains information about a CDN_INCLUDEITEM notification message. |
| [_OFNOTIFYEXW structure](..\commdlg\ns-commdlg-_ofnotifyexw.md) | Contains information about a CDN_INCLUDEITEM notification message. |
| [_OFNOTIFYW structure](..\commdlg\ns-commdlg-_ofnotifyw.md) | Contains information about a WM_NOTIFY message sent to an OFNHookProc hook procedure for an Open or Save As dialog box. The lParam parameter of the WM_NOTIFY message is a pointer to an OFNOTIFY structure. |
| [tagCHOOSECOLORA structure](..\commdlg\ns-commdlg-tagchoosecolora.md) | Contains information the ChooseColor function uses to initialize the Color dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagCHOOSECOLORW structure](..\commdlg\ns-commdlg-tagchoosecolorw.md) | Contains information the ChooseColor function uses to initialize the Color dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagCHOOSEFONTA structure](..\commdlg\ns-commdlg-tagchoosefonta.md) | Contains information that the ChooseFont function uses to initialize the Font dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagCHOOSEFONTW structure](..\commdlg\ns-commdlg-tagchoosefontw.md) | Contains information that the ChooseFont function uses to initialize the Font dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagDEVNAMES structure](..\commdlg\ns-commdlg-tagdevnames.md) | Contains strings that identify the driver, device, and output port names for a printer. |
| [tagFINDREPLACEA structure](..\commdlg\ns-commdlg-tagfindreplacea.md) | Contains information that the FindText and ReplaceText functions use to initialize the Find and Replace dialog boxes. |
| [tagFINDREPLACEW structure](..\commdlg\ns-commdlg-tagfindreplacew.md) | Contains information that the FindText and ReplaceText functions use to initialize the Find and Replace dialog boxes. |
| [tagOFNA structure](..\commdlg\ns-commdlg-tagofna.md) | Contains information that the GetOpenFileName and GetSaveFileName functions use to initialize an Open or Save As dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagOFNW structure](..\commdlg\ns-commdlg-tagofnw.md) | Contains information that the GetOpenFileName and GetSaveFileName functions use to initialize an Open or Save As dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure. |
| [tagOFN_NT4A structure](..\commdlg\ns-commdlg-tagofn_nt4a.md) | The OPENFILENAME_NT4 structure is identical to OPENFILENAME with _WIN32_WINNT set to 0x0400. |
| [tagOFN_NT4W structure](..\commdlg\ns-commdlg-tagofn_nt4w.md) | The OPENFILENAME_NT4 structure is identical to OPENFILENAME with _WIN32_WINNT set to 0x0400. |
| [tagPDA structure](..\commdlg\ns-commdlg-tagpda.md) | Contains information that the PrintDlg function uses to initialize the Print Dialog Box. After the user closes the dialog box, the system uses this structure to return information about the user's selections. |
| [tagPDEXA structure](..\commdlg\ns-commdlg-tagpdexa.md) | Contains information that the PrintDlgEx function uses to initialize the Print property sheet. After the user closes the property sheet, the system uses this structure to return information about the user's selections. |
| [tagPDEXW structure](..\commdlg\ns-commdlg-tagpdexw.md) | Contains information that the PrintDlgEx function uses to initialize the Print property sheet. After the user closes the property sheet, the system uses this structure to return information about the user's selections. |
| [tagPDW structure](..\commdlg\ns-commdlg-tagpdw.md) | Contains information that the PrintDlg function uses to initialize the Print Dialog Box. After the user closes the dialog box, the system uses this structure to return information about the user's selections. |
| [tagPRINTPAGERANGE structure](..\commdlg\ns-commdlg-tagprintpagerange.md) | Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the PRINTDLGEX structure when calling the PrintDlgEx function. |
| [tagPSDA structure](..\commdlg\ns-commdlg-tagpsda.md) | Contains information the PageSetupDlg function uses to initialize the Page Setup dialog box. After the user closes the dialog box, the system returns information about the user-defined page parameters in this structure. |
| [tagPSDW structure](..\commdlg\ns-commdlg-tagpsdw.md) | Contains information the PageSetupDlg function uses to initialize the Page Setup dialog box. After the user closes the dialog box, the system returns information about the user-defined page parameters in this structure. |
