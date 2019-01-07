---
UID: NF:windowsx.Button_SetCheck
title: Button_SetCheck macro
author: windows-sdk-content
description: Sets the check state of a radio button or check box. You can use this macro or send the BM_SETCHECK message explicitly.
old-location: controls\Button_SetCheck.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setcheck.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BST_CHECKED, BST_INDETERMINATE, BST_UNCHECKED, Button_SetCheck, Button_SetCheck macro [Windows Controls], _win32_Button_SetCheck, _win32_Button_SetCheck_cpp, controls.Button_SetCheck, controls._win32_Button_SetCheck, windowsx/Button_SetCheck
ms.topic: macro
req.header: windowsx.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Button_SetCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetCheck macro


## -description


Sets the check state of a radio button or check box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775989(v=VS.85).aspx">BM_SETCHECK</a> message explicitly. 



## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param check

Type: <b>int</b>

The check state. This parameter can be one of the following values. 

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
Sets the button state to cleared.

</td>
</tr>
</table>
 


## -remarks



The macro has no effect on push buttons. 



