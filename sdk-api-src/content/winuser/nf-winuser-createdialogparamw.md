---
UID: NF:winuser.CreateDialogParamW
title: CreateDialogParamW function (winuser.h)
description: Creates a modeless dialog box from a dialog box template resource. (Unicode)
helpviewer_keywords: ["CreateDialogParam", "CreateDialogParam function [Dialog Boxes]", "CreateDialogParamW", "_win32_CreateDialogParam", "_win32_createdialogparam_cpp", "dlgbox.createdialogparam", "winui._win32_createdialogparam", "winuser/CreateDialogParam", "winuser/CreateDialogParamW"]
old-location: dlgbox\createdialogparam.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\createdialogparam.htm
ms.date: 12/05/2018
ms.keywords: CreateDialogParam, CreateDialogParam function [Dialog Boxes], CreateDialogParamA, CreateDialogParamW, _win32_CreateDialogParam, _win32_createdialogparam_cpp, dlgbox.createdialogparam, winui._win32_createdialogparam, winuser/CreateDialogParam, winuser/CreateDialogParamA, winuser/CreateDialogParamW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDialogParamW (Unicode) and CreateDialogParamA (ANSI)
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
 - CreateDialogParamW
 - winuser/CreateDialogParamW
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
 - CreateDialogParam
 - CreateDialogParamA
 - CreateDialogParamW
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# CreateDialogParamW function


## -description

Creates a modeless dialog box from a dialog box template resource. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the <i>lParam</i> parameter of the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. An application can use this value to initialize dialog box controls.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module which contains the dialog box template. If this parameter is NULL, then the current executable is used.

### -param lpTemplateName [in]

Type: <b>LPCTSTR</b>

The dialog box template. This parameter is either the pointer to a null-terminated character string that specifies the name of the dialog box template or an integer value that specifies the resource identifier of the dialog box template. If the parameter specifies a resource identifier, its high-order word must be zero and low-order word must contain the identifier. You can use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro to create this value.

### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the dialog box.

### -param lpDialogFunc [in, optional]

Type: <b>DLGPROC</b>

A pointer to the dialog box procedure. For more information about the dialog box procedure, see <a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>.

### -param dwInitParam [in]

Type: <b>LPARAM</b>

The value to be passed to the dialog box procedure in the <i>lParam</i> parameter in the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the window handle to the dialog box.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CreateDialogParam</b> function uses the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function to create the dialog box. <b>CreateDialogParam</b> then sends a <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message (and a <a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a> message if the template specifies the <a href="/windows/desktop/dlgbox/about-dialog-boxes">DS_SETFONT</a> or DS_SHELLFONT style) to the dialog box procedure. The function displays the dialog box if the template specifies the <b>WS_VISIBLE</b> style. Finally, <b>CreateDialogParam</b> returns the window handle of the dialog box. 

After <b>CreateDialogParam</b> returns, the application displays the dialog box (if it is not already displayed) using the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function. The application destroys the dialog box by using the <a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a> function. To support keyboard navigation and other dialog box functionality, the message loop for the dialog box must call the <a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a> function.





> [!NOTE]
> The winuser.h header defines CreateDialogParam as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirecta">CreateDialogIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirectparama">CreateDialogIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nc-winuser-dlgproc">DialogProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isdialogmessagea">IsDialogMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/winmsg/wm-setfont">WM_SETFONT</a>
