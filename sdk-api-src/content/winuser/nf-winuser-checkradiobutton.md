---
UID: NF:winuser.CheckRadioButton
title: CheckRadioButton function (winuser.h)
description: Adds a check mark to (checks) a specified radio button in a group and removes a check mark from (clears) all other radio buttons in the group.
helpviewer_keywords: ["CheckRadioButton","CheckRadioButton function [Windows Controls]","_win32_CheckRadioButton","_win32_CheckRadioButton_cpp","controls.CheckRadioButton","controls._win32_CheckRadioButton","winuser/CheckRadioButton"]
old-location: controls\CheckRadioButton.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonfunctions\checkradiobutton.htm
ms.date: 12/05/2018
ms.keywords: CheckRadioButton, CheckRadioButton function [Windows Controls], _win32_CheckRadioButton, _win32_CheckRadioButton_cpp, controls.CheckRadioButton, controls._win32_CheckRadioButton, winuser/CheckRadioButton
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CheckRadioButton
 - winuser/CheckRadioButton
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
 - CheckRadioButton
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# CheckRadioButton function


## -description

Adds a check mark to (checks) a specified radio button in a group and removes a check mark from (clears) all other radio buttons in the group.

## -parameters

### -param hDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the radio button.

### -param nIDFirstButton [in]

Type: <b>int</b>

The identifier of the first radio button in the group.

### -param nIDLastButton [in]

Type: <b>int</b>

The identifier of the last radio button in the group.

### -param nIDCheckButton [in]

Type: <b>int</b>

The identifier of the radio button to select.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CheckRadioButton</b> function sends a <a href="/windows/desktop/Controls/bm-setcheck">BM_SETCHECK</a> message to each of the radio buttons in the indicated group.

The <i>nIDFirstButton</i> and <i>nIDLastButton</i> parameters specify a range of button identifiers (normally the resource IDs of the buttons).  The position of buttons in the tab order is irrelevant; if a button forms part of a group, but has an ID outside the specified range, it is not affected by this call.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-checkdlgbutton">CheckDlgButton</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isdlgbuttonchecked">IsDlgButtonChecked</a>



<b>Reference</b>
