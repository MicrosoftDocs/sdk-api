---
UID: NF:commdlg.FindTextW
title: FindTextW function (commdlg.h)
description: Creates a system-defined modeless Find dialog box that lets the user specify a string to search for and options to use when searching for text in a document. (Unicode)
helpviewer_keywords: ["FindText", "FindText function [Dialog Boxes]", "FindTextW", "_win32_FindText", "_win32_findtext_cpp", "commdlg/FindText", "commdlg/FindTextW", "dlgbox.findtext", "winui._win32_findtext"]
old-location: dlgbox\findtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\findtext.htm
ms.date: 12/05/2018
ms.keywords: FindText, FindText function [Dialog Boxes], FindTextA, FindTextW, _win32_FindText, _win32_findtext_cpp, commdlg/FindText, commdlg/FindTextA, commdlg/FindTextW, dlgbox.findtext, winui._win32_findtext
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindTextW (Unicode) and FindTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindTextW
 - commdlg/FindTextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comdlg32.dll
api_name:
 - FindText
 - FindTextA
 - FindTextW
req.apiset: ext-ms-win-shell-comdlg32-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# FindTextW function


## -description

Creates a system-defined modeless <b>Find</b> dialog box that lets the user specify a string to search for and options to use when searching for text in a document.

## -parameters

### -param unnamedParam1 [in]

Type: <b>LPFINDREPLACE</b>

A pointer to a <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure that contains information used to initialize the dialog box. The dialog box uses this structure to send information about the user's input to your application. For more information, see the following Remarks section.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box. You can use the window handle to communicate with or to close the dialog box.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call the <a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a> function. <b>CommDlgExtendedError</b> may return one of the following error codes:

## -remarks

The <b>FindText</b> function does not perform a search operation. Instead, the dialog box sends <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> registered messages to the window procedure of the owner window of the dialog box. When you create the dialog box, the  <b>hwndOwner</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure is a handle to the owner window.

Before calling <b>FindText</b>, you must call the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to get the identifier for the <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message. The dialog box procedure uses this identifier to send messages when the user clicks the <b>Find Next</b> button, or when the dialog box is closing. The  <i>lParam</i> parameter of the <b>FINDMSGSTRING</b> message contains a pointer to a <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure. The  <b>Flags</b> member of this structure indicates the event that caused the message. Other members of the structure indicate the user's input.

If you create a <b>Find</b> dialog box, you must also use the <a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a> function in the main message loop of your application to ensure that the dialog box correctly processes keyboard input, such as the TAB and ESC keys. <b>IsDialogMessage</b> returns a value that indicates whether the <b>Find</b> dialog box processed the message.

You can provide an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a> hook procedure for a <b>Find</b> dialog box. The hook procedure can process messages sent to the dialog box. To enable a hook procedure, set the <b>FR_ENABLEHOOK</b> flag in the  <b>Flags</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-common-dialog-boxes">Finding Text</a>.

<div class="code"></div>




> [!NOTE]
> The commdlg.h header defines FindText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a>



<a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/commdlg/nf-commdlg-replacetexta">ReplaceText</a>
