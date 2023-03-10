---
UID: NF:winuser.EndDialog
title: EndDialog function (winuser.h)
description: Destroys a modal dialog box, causing the system to end any processing for the dialog box.
helpviewer_keywords: ["EndDialog","EndDialog function [Dialog Boxes]","_win32_EndDialog","_win32_enddialog_cpp","dlgbox.enddialog","winui._win32_enddialog","winuser/EndDialog"]
old-location: dlgbox\enddialog.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\enddialog.htm
ms.date: 12/05/2018
ms.keywords: EndDialog, EndDialog function [Dialog Boxes], _win32_EndDialog, _win32_enddialog_cpp, dlgbox.enddialog, winui._win32_enddialog, winuser/EndDialog
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - EndDialog
 - winuser/EndDialog
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
 - EndDialog
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# EndDialog function


## -description

Destroys a modal dialog box, causing the system to end any processing for the dialog box.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box to be destroyed.

### -param nResult [in]

Type: <b>INT_PTR</b>

The value to be returned to the application from the function that created the dialog box.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Dialog boxes created by the <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>, <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxparama">DialogBoxParam</a>, <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a> functions must be destroyed using the <b>EndDialog</b> function. An application calls <b>EndDialog</b> from within the dialog box procedure; the function must not be used for any other purpose. 

A dialog box procedure can call <b>EndDialog</b> at any time, even during the processing of the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. If your application calls the function while <b>WM_INITDIALOG</b> is being processed, the dialog box is destroyed before it is shown and before the input focus is set. 

<b>EndDialog</b> does not destroy the dialog box immediately. Instead, it sets a flag and allows the dialog box procedure to return control to the system. The system checks the flag before attempting to retrieve the next message from the application queue. If the flag is set, the system ends the message loop, destroys the dialog box, and uses the value in <i>nResult</i> as the return value from the function that created the dialog box.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxparama">DialogBoxParam</a>



<b>Reference</b>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
