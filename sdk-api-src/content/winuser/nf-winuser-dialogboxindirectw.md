---
UID: NF:winuser.DialogBoxIndirectW
title: DialogBoxIndirectW macro (winuser.h)
description: Creates a modal dialog box from a dialog box template in memory. DialogBoxIndirect does not return control until the specified callback function terminates the modal dialog box by calling the EndDialog function. (Unicode)
helpviewer_keywords: ["DialogBoxIndirect", "DialogBoxIndirect function [Dialog Boxes]", "DialogBoxIndirectW", "_win32_DialogBoxIndirect", "_win32_dialogboxindirect_cpp", "dlgbox.dialogboxindirect", "winui._win32_dialogboxindirect", "winuser/DialogBoxIndirect", "winuser/DialogBoxIndirectW"]
old-location: dlgbox\dialogboxindirect.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogboxindirect.htm
ms.date: 12/05/2018
ms.keywords: DialogBoxIndirect, DialogBoxIndirect function [Dialog Boxes], DialogBoxIndirectA, DialogBoxIndirectW, _win32_DialogBoxIndirect, _win32_dialogboxindirect_cpp, dlgbox.dialogboxindirect, winui._win32_dialogboxindirect, winuser/DialogBoxIndirect, winuser/DialogBoxIndirectA, winuser/DialogBoxIndirectW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DialogBoxIndirectW (Unicode) and DialogBoxIndirectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DialogBoxIndirectW
 - winuser/DialogBoxIndirectW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DialogBoxIndirect
 - DialogBoxIndirectA
 - DialogBoxIndirectW
---

# DialogBoxIndirectW macro


## -description

Creates a modal dialog box from a dialog box template in memory. <b>DialogBoxIndirect</b> does not return control until the specified callback function terminates the modal dialog box by calling the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function.

<b>DialogBoxIndirect</b> is implemented as a call to the <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a> function.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module that creates the dialog box.

### -param lpTemplate [in]

Type: <b>LPCDLGTEMPLATE</b>

The template that <b>DialogBoxIndirect</b> uses to create the dialog box. A dialog box template consists of a header that describes the dialog box, followed by one or more additional blocks of data that describe each of the controls in the dialog box. The template can use either the standard format or the extended format. 
					

In a standard template for a dialog box, the header is a <a href="/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a> structure followed by additional variable-length arrays. The data for each control consists of a <a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a> structure followed by additional variable-length arrays. 

In an extended template for a dialog box, the header uses the <a href="/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> format and the control definitions use the <a href="/windows/desktop/dlgbox/dlgitemtemplateex">DLGITEMTEMPLATEEX</a> format.

### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box.

### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>.

## -remarks

The <b>DialogBoxIndirect</b> macro uses the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function to create the dialog box. <b>DialogBoxIndirect</b> then sends a <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message to the dialog box procedure. If the template specifies the <a href="/windows/desktop/dlgbox/about-dialog-boxes">DS_SETFONT</a> or DS_SHELLFONT style, the function also sends a <a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a> message to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function, <b>DialogBoxIndirect</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 

In a standard dialog box template, the <a href="/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a> structure and each of the <a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a> structures must be aligned on <b>DWORD</b> boundaries. The creation data array that follows a <b>DLGITEMTEMPLATE</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

In an extended dialog box template, the <a href="/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a> header and each of the <a href="/windows/desktop/dlgbox/dlgitemtemplateex">DLGITEMTEMPLATEEX</a> control definitions must be aligned on <b>DWORD</b> boundaries. The creation data array, if any, that follows a <b>DLGITEMTEMPLATEEX</b> structure must also be aligned on a <b>DWORD</b> boundary. All of the other variable-length arrays in the template must be aligned on <b>WORD</b> boundaries. 

All character strings in the dialog box template, such as titles for the dialog box and buttons, must be Unicode strings. Use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function to generate Unicode strings from ANSI strings.


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Creating a Template in Memory</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines DialogBoxIndirect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate">DLGITEMTEMPLATE</a>



<a href="/windows/desktop/dlgbox/dlgitemtemplateex">DLGITEMTEMPLATEEX</a>



<a href="/windows/desktop/api/winuser/ns-winuser-dlgtemplate">DLGTEMPLATE</a>



<a href="/windows/desktop/dlgbox/dlgtemplateex">DLGTEMPLATEEX</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxparama">DialogBoxParam</a>



<a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a>
