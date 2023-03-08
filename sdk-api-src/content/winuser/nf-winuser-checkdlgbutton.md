---
UID: NF:winuser.CheckDlgButton
title: CheckDlgButton function (winuser.h)
description: Changes the check state of a button control.
helpviewer_keywords: ["BST_CHECKED","BST_INDETERMINATE","BST_UNCHECKED","CheckDlgButton","CheckDlgButton function [Windows Controls]","_win32_CheckDlgButton","_win32_CheckDlgButton_cpp","controls.CheckDlgButton","controls._win32_CheckDlgButton","winuser/CheckDlgButton"]
old-location: controls\CheckDlgButton.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonfunctions\checkdlgbutton.htm
ms.date: 12/05/2018
ms.keywords: BST_CHECKED, BST_INDETERMINATE, BST_UNCHECKED, CheckDlgButton, CheckDlgButton function [Windows Controls], _win32_CheckDlgButton, _win32_CheckDlgButton_cpp, controls.CheckDlgButton, controls._win32_CheckDlgButton, winuser/CheckDlgButton
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
 - CheckDlgButton
 - winuser/CheckDlgButton
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
 - CheckDlgButton
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# CheckDlgButton function


## -description

Changes the check state of a button control.

## -parameters

### -param hDlg [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the dialog box that contains the button.

### -param nIDButton [in]

Type: <b>int</b>

The identifier of the button to modify.

### -param uCheck [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The check state of the button. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BST_CHECKED"></a><a id="bst_checked"></a><dl>
<dt><b>BST_CHECKED</b></dt>
</dl>
</td>
<td width="60%">
Sets the button state to checked.

</td>
</tr>
<tr>
<td width="40%"><a id="BST_INDETERMINATE"></a><a id="bst_indeterminate"></a><dl>
<dt><b>BST_INDETERMINATE</b></dt>
</dl>
</td>
<td width="60%">
Sets the button state to grayed, indicating an indeterminate state. Use this value only if the button has the <a href="/windows/desktop/Controls/button-styles">BS_3STATE</a> or <a href="/windows/desktop/Controls/button-styles">BS_AUTO3STATE</a> style.

</td>
</tr>
<tr>
<td width="40%"><a id="BST_UNCHECKED"></a><a id="bst_unchecked"></a><dl>
<dt><b>BST_UNCHECKED</b></dt>
</dl>
</td>
<td width="60%">
Sets the button state to cleared

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CheckDlgButton</b> function sends a 
				<a href="/windows/desktop/Controls/bm-setcheck">BM_SETCHECK</a> message to the specified button control in the specified dialog box.


#### Examples

For an example, see <b>Creating a Modeless Dialog Box</b> in <a href="/windows/desktop/dlgbox/using-dialog-boxes">Using Dialog Boxes</a>. 

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-checkradiobutton">CheckRadioButton</a>



<a href="/windows/desktop/api/winuser/nf-winuser-isdlgbuttonchecked">IsDlgButtonChecked</a>



<b>Reference</b>
