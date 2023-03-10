---
UID: NF:winuser.IsDlgButtonChecked
title: IsDlgButtonChecked function (winuser.h)
description: The IsDlgButtonChecked function determines whether a button control is checked or whether a three-state button control is checked, unchecked, or indeterminate.
helpviewer_keywords: ["IsDlgButtonChecked","IsDlgButtonChecked function [Windows Controls]","_win32_IsDlgButtonChecked","_win32_IsDlgButtonChecked_cpp","controls.IsDlgButtonChecked","controls._win32_IsDlgButtonChecked","winuser/IsDlgButtonChecked"]
old-location: controls\IsDlgButtonChecked.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonfunctions\isdlgbuttonchecked.htm
ms.date: 12/05/2018
ms.keywords: IsDlgButtonChecked, IsDlgButtonChecked function [Windows Controls], _win32_IsDlgButtonChecked, _win32_IsDlgButtonChecked_cpp, controls.IsDlgButtonChecked, controls._win32_IsDlgButtonChecked, winuser/IsDlgButtonChecked
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
 - IsDlgButtonChecked
 - winuser/IsDlgButtonChecked
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
 - IsDlgButtonChecked
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# IsDlgButtonChecked function


## -description

The <b>IsDlgButtonChecked</b> function determines whether a button control is checked or whether a three-state button control is checked, unchecked, or indeterminate.

## -parameters

### -param hDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the button control.

### -param nIDButton [in]

Type: <b>int</b>

The identifier of the button control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The return value from a button created with the <a href="/windows/desktop/Controls/button-styles">BS_AUTOCHECKBOX</a>, <a href="/windows/desktop/Controls/button-styles">BS_AUTORADIOBUTTON</a>, <a href="/windows/desktop/Controls/button-styles">BS_AUTO3STATE</a>, <a href="/windows/desktop/Controls/button-styles">BS_CHECKBOX</a>, <a href="/windows/desktop/Controls/button-styles">BS_RADIOBUTTON</a>, or <a href="/windows/desktop/Controls/button-styles">BS_3STATE</a> styles can be one of the values in the following table. If the button has any other style, the return value is zero. 
				

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BST_CHECKED</b></dt>
</dl>
</td>
<td width="60%">
The button is checked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BST_INDETERMINATE</b></dt>
</dl>
</td>
<td width="60%">
The button is in an indeterminate state (applies only if the button has the <a href="/windows/desktop/Controls/button-styles">BS_3STATE</a> or <a href="/windows/desktop/Controls/button-styles">BS_AUTO3STATE</a> style).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BST_UNCHECKED</b></dt>
</dl>
</td>
<td width="60%">
The button is not checked.

</td>
</tr>
</table>

## -remarks

The <b>IsDlgButtonChecked</b> function sends a <a href="/windows/desktop/Controls/bm-getcheck">BM_GETCHECK</a> message to the specified button control. 


#### Examples

For an example, see the section titled "Creating a Modeless Dialog Box" in <a href="/windows/desktop/dlgbox/using-dialog-boxes">Using Dialog Boxes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-checkdlgbutton">CheckDlgButton</a>
