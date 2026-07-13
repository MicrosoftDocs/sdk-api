---
UID: NF:commdlg.ReplaceTextW
title: ReplaceTextW function (commdlg.h)
description: Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations. (Unicode)
helpviewer_keywords: ["ReplaceText", "ReplaceText function [Dialog Boxes]", "ReplaceTextW", "_win32_ReplaceText", "_win32_replacetext_cpp", "commdlg/ReplaceText", "commdlg/ReplaceTextW", "dlgbox.replacetext", "winui._win32_replacetext"]
old-location: dlgbox\replacetext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxfunctions\replacetext.htm
ms.date: 12/05/2018
ms.keywords: ReplaceText, ReplaceText function [Dialog Boxes], ReplaceTextA, ReplaceTextW, _win32_ReplaceText, _win32_replacetext_cpp, commdlg/ReplaceText, commdlg/ReplaceTextA, commdlg/ReplaceTextW, dlgbox.replacetext, winui._win32_replacetext
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReplaceTextW (Unicode) and ReplaceTextA (ANSI)
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
 - ReplaceTextW
 - commdlg/ReplaceTextW
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
 - ReplaceText
 - ReplaceTextA
 - ReplaceTextW
req.apiset: ext-ms-win-shell-comdlg32-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# ReplaceTextW function


## -description

Creates a system-defined modeless dialog box that lets the user specify a string to search for and a replacement string, as well as options to control the find and replace operations.

## -parameters

### -param unnamedParam1 [in, out]

Type: <b>LPFINDREPLACE</b>

A pointer to a <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure that contains information used to initialize the dialog box. The dialog box uses this structure to send information about the user's input to your application. For more information, see the following Remarks section.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box. You can use the window handle to communicate with the dialog box or close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call the <a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a> function, which can return one of the following error codes:

## -remarks

The <b>ReplaceText</b> function does not perform a text replacement operation. Instead, the dialog box sends <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> registered messages to the window procedure of the owner window of the dialog box. When you create the dialog box, the  <b>hwndOwner</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure is a handle to the owner window.

Before calling <b>ReplaceText</b>, you must call the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to get the identifier for the <a href="/windows/desktop/dlgbox/findmsgstring">FINDMSGSTRING</a> message. The dialog box procedure uses this identifier to send messages when the user clicks the <b>Find Next</b>, <b>Replace</b>, or <b>Replace All</b> buttons, or when the dialog box is closing. The  <i>lParam</i> parameter of a <b>FINDMSGSTRING</b> message contains a pointer to the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure. The  <b>Flags</b> member of this structure indicates the event that caused the message. Other members of the structure indicate the user's input.

If you create a <b>Replace</b> dialog box, you must also use the <a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a> function in the main message loop of your application to ensure that the dialog box correctly processes keyboard input, such as the TAB and ESC keys. The <b>IsDialogMessage</b> function returns a value that indicates whether the Replace dialog box processed the message.

You can provide an <a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a> hook procedure for a <b>Replace</b> dialog box. The hook procedure can process messages sent to the dialog box. To enable a hook procedure, set the <b>FR_ENABLEHOOK</b> flag in the  <b>Flags</b> member of the <a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a> structure and specify the address of the hook procedure in the  <b>lpfnHook</b> member.





> [!NOTE]
> The commdlg.h header defines ReplaceText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/commdlg/nf-commdlg-commdlgextendederror">CommDlgExtendedError</a>



<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/ns-commdlg-findreplacea">FINDREPLACE</a>



<a href="/windows/desktop/api/commdlg/nc-commdlg-lpfrhookproc">FRHookProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a>
