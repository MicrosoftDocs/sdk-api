---
UID: NF:winuser.SetDlgItemInt
title: SetDlgItemInt function (winuser.h)
description: Sets the text of a control in a dialog box to the string representation of a specified integer value.
helpviewer_keywords: ["SetDlgItemInt","SetDlgItemInt function [Dialog Boxes]","_win32_SetDlgItemInt","_win32_setdlgitemint_cpp","dlgbox.setdlgitemint","winui._win32_setdlgitemint","winuser/SetDlgItemInt"]
old-location: dlgbox\setdlgitemint.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\setdlgitemint.htm
ms.date: 12/05/2018
ms.keywords: SetDlgItemInt, SetDlgItemInt function [Dialog Boxes], _win32_SetDlgItemInt, _win32_setdlgitemint_cpp, dlgbox.setdlgitemint, winui._win32_setdlgitemint, winuser/SetDlgItemInt
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
 - SetDlgItemInt
 - winuser/SetDlgItemInt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - SetDlgItemInt
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# SetDlgItemInt function


## -description

Sets the text of a control in a dialog box to the string representation of a specified integer value.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control.

### -param nIDDlgItem [in]

Type: <b>int</b>

The control to be changed.

### -param uValue [in]

Type: <b>UINT</b>

The integer value used to generate the item text.

### -param bSigned [in]

Type: <b>BOOL</b>

Indicates whether the <i>uValue</i> parameter is signed or unsigned. If this parameter is <b>TRUE</b>, <i>uValue</i> is signed. If this parameter is <b>TRUE</b> and <i>uValue</i> is less than zero, a minus sign is placed before the first digit in the string. If this parameter is <b>FALSE</b>, <i>uValue</i> is unsigned.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To set the new text, this function sends a <a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a> message to the specified control.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint">GetDlgItemInt</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta">SetDlgItemText</a>



<a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a>
