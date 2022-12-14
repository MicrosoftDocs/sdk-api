---
UID: NC:winuser.DLGPROC
title: DLGPROC (winuser.h)
description: Application-defined callback function used with the CreateDialog and DialogBox families of functions.
helpviewer_keywords: ["DLGPROC","DLGPROC callback","DLGPROC callback function [Dialog Boxes]","_win32_DialogProc","_win32_dialogproc_cpp","dlgbox.dialogproc","winui._win32_dialogproc","winuser/DLGPROC"]
old-location: dlgbox\dialogproc.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\dialogproc.htm
ms.date: 12/05/2018
ms.keywords: DLGPROC, DLGPROC callback, DLGPROC callback function [Dialog Boxes], _win32_DialogProc, _win32_dialogproc_cpp, dlgbox.dialogproc, winui._win32_dialogproc, winuser/DLGPROC
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DLGPROC
 - winuser/DLGPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - DLGPROC
---

# DLGPROC callback function


## -description

Application-defined callback function used with the <a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a> and <a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a> families of functions. It processes messages sent to a modal or modeless dialog box. The <b>DLGPROC</b> type defines a pointer to this callback function. <i>DialogProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: <b>HWND</b>

A handle to the dialog box.

### -param unnamedParam2

Type: <b>UINT</b>

The message.

### -param unnamedParam3

Type: <b>WPARAM</b>

Additional message-specific information.

### -param unnamedParam4

Type: <b>LPARAM</b>

Additional message-specific information. 



Type: <b>INT_PTR</b>

Typically, the dialog box procedure should return <b>TRUE</b> if it processed the message, and <b>FALSE</b> if it did not. If the dialog box procedure returns <b>FALSE</b>, the dialog manager performs the default dialog operation in response to the message.

If the dialog box procedure processes a message that requires a specific return value, the dialog box procedure should set the desired return value by calling <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>(<i>hwndDlg</i>, <b>DWL_MSGRESULT</b>, <i>lResult</i>) immediately before returning <b>TRUE</b>. Note that you must call <b>SetWindowLong</b> immediately before returning <b>TRUE</b>; doing so earlier may result in the <b>DWL_MSGRESULT</b> value being overwritten by a nested dialog box message.

The following messages are exceptions to the general rules stated above. Consult the documentation for the specific message for details on the semantics of the return value.

<ul>
<li>
<a href="/windows/desktop/Controls/wm-chartoitem">WM_CHARTOITEM</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-compareitem">WM_COMPAREITEM</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-ctlcolorbtn">WM_CTLCOLORBTN</a>
</li>
<li>
<a href="/windows/desktop/dlgbox/wm-ctlcolordlg">WM_CTLCOLORDLG</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-ctlcoloredit">WM_CTLCOLOREDIT</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-ctlcolorlistbox">WM_CTLCOLORLISTBOX</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-ctlcolorscrollbar">WM_CTLCOLORSCROLLBAR</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-ctlcolorstatic">WM_CTLCOLORSTATIC</a>
</li>
<li>
<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>
</li>
<li>
<a href="/windows/desktop/winmsg/wm-querydragicon">WM_QUERYDRAGICON</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-vkeytoitem">WM_VKEYTOITEM</a>
</li>
</ul>

## -remarks

You should use the dialog box procedure only if you use the dialog box class for the dialog box. This is the default class and is used when no explicit class is specified in the dialog box template. Although the dialog box procedure is similar to a window procedure, it must not call the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process unwanted messages. Unwanted messages are processed internally by the dialog box window procedure.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialoga">CreateDialog</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirecta">CreateDialogIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogindirectparama">CreateDialogIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdialogparama">CreateDialogParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxa">DialogBox</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirecta">DialogBoxIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxindirectparama">DialogBoxIndirectParam</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dialogboxparama">DialogBoxParam</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setfocus">SetFocus</a>



<a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a>