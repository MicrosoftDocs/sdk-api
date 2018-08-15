---
UID: NF:winuser.CheckDlgButton
title: CheckDlgButton function
author: windows-sdk-content
description: Changes the check state of a button control.
old-location: controls\CheckDlgButton.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonfunctions\checkdlgbutton.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BST_CHECKED, BST_INDETERMINATE, BST_UNCHECKED, CheckDlgButton, CheckDlgButton function [Windows Controls], _win32_CheckDlgButton, _win32_CheckDlgButton_cpp, controls.CheckDlgButton, controls._win32_CheckDlgButton, winuser/CheckDlgButton
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CheckDlgButton function


## -description


Changes the check state of a button control.


## -parameters




### -param hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the button. 


### -param nIDButton [in]

Type: <b>int</b>

The identifier of the button to modify. 


### -param uCheck [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

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
Sets the button state to grayed, indicating an indeterminate state. Use this value only if the button has the <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_3STATE</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_AUTO3STATE</a> style.

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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CheckDlgButton</b> function sends a 
				<a href="https://msdn.microsoft.com/en-us/library/Bb775989(v=VS.85).aspx">BM_SETCHECK</a> message to the specified button control in the specified dialog box.


#### Examples

For an example, see <b>Creating a Modeless Dialog Box</b> in <a href="https://msdn.microsoft.com/en-us/library/ms644996(v=VS.85).aspx">Using Dialog Boxes</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761877(v=VS.85).aspx">CheckRadioButton</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761879(v=VS.85).aspx">IsDlgButtonChecked</a>



<b>Reference</b>
 

 

