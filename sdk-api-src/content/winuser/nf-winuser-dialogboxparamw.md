---
UID: NF:winuser.DialogBoxParamW
title: DialogBoxParamW function (winuser.h)
description: Creates a modal dialog box from a dialog box template resource. (Unicode)
helpviewer_keywords: ["DialogBoxParam", "DialogBoxParam function [Dialog Boxes]", "DialogBoxParamW", "_win32_DialogBoxParam", "_win32_dialogboxparam_cpp", "dlgbox.dialogboxparam", "winui._win32_dialogboxparam", "winuser/DialogBoxParam", "winuser/DialogBoxParamW"]
old-location: dlgbox\dialogboxparam.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogboxparam.htm
ms.date: 12/05/2018
ms.keywords: DialogBoxParam, DialogBoxParam function [Dialog Boxes], DialogBoxParamA, DialogBoxParamW, _win32_DialogBoxParam, _win32_dialogboxparam_cpp, dlgbox.dialogboxparam, winui._win32_dialogboxparam, winuser/DialogBoxParam, winuser/DialogBoxParamA, winuser/DialogBoxParamW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DialogBoxParamW (Unicode) and DialogBoxParamA (ANSI)
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
 - DialogBoxParamW
 - winuser/DialogBoxParamW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - DialogBoxParam
 - DialogBoxParamA
 - DialogBoxParamW
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-1 (introduced in Windows 8.1)
---

# DialogBoxParamW function


## -description

Creates a modal dialog box from a dialog box template resource. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the <i>lParam</i> parameter of the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. An application can use this value to initialize dialog box controls.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.

### -param lpTemplateName [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and its low-order word must contain the identifier. You can use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro to create this value.

### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box.

### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>.

### -param dwInitParam [in]

Type: <b>LPARAM</b>

The value to pass to the dialog box in the <i>lParam</i> parameter of the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

## -returns

Type: <b>INT_PTR</b>

If the function succeeds, the return value is the value of the <i>nResult</i> parameter specified in the call to the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function used to terminate the dialog box.

If the function fails because the <i>hWndParent</i> parameter is invalid, the return value is zero. The function returns zero in this case for compatibility with previous versions of Windows. If the function fails for any other reason, the return value is –1. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DialogBoxParam</b> function uses the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function to create the dialog box. <b>DialogBoxParam</b> then sends a <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message (and a <a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a> message if the template specifies the <a href="/windows/desktop/dlgbox/about-dialog-boxes">DS_SETFONT</a> or DS_SHELLFONT style) to the dialog box procedure. The function displays the dialog box (regardless of whether the template specifies the <b>WS_VISIBLE</b> style), disables the owner window, and starts its own message loop to retrieve and dispatch messages for the dialog box. 

When the dialog box procedure calls the <a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a> function, <b>DialogBoxParam</b> destroys the dialog box, ends the message loop, enables the owner window (if previously enabled), and returns the <i>nResult</i> parameter specified by the dialog box procedure when it called <b>EndDialog</b>. 





> [!NOTE]
> The winuser.h header defines DialogBoxParam as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enddialog">EndDialog</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a>
