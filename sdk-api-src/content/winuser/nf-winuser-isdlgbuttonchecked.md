---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IsDlgButtonChecked function


## -description


The <b>IsDlgButtonChecked</b> function determines whether a button control is checked or whether a three-state button control is checked, unchecked, or indeterminate. 


## -parameters




### -param hDlg [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the dialog box that contains the button control. 


### -param nIDButton [in]

Type: <b>int</b>

The identifier of the button control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The return value from a button created with the <a href="Button_Styles.htm">BS_AUTOCHECKBOX</a>, <a href="Button_Styles.htm">BS_AUTORADIOBUTTON</a>, <a href="Button_Styles.htm">BS_AUTO3STATE</a>, <a href="Button_Styles.htm">BS_CHECKBOX</a>, <a href="Button_Styles.htm">BS_RADIOBUTTON</a>, or <a href="Button_Styles.htm">BS_3STATE</a> styles can be one of the values in the following table. If the button has any other style, the return value is zero. 
				

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
The button is in an indeterminate state (applies only if the button has the <a href="Button_Styles.htm">BS_3STATE</a> or <a href="Button_Styles.htm">BS_AUTO3STATE</a> style).

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



The <b>IsDlgButtonChecked</b> function sends a <a href="https://msdn.microsoft.com/a25b2c8d-0b32-4807-bfb4-e277675924f1">BM_GETCHECK</a> message to the specified button control. 


#### Examples

For an example, see the section titled "Creating a Modeless Dialog Box" in <a href="https://msdn.microsoft.com/8a5b6bdd-4429-4f48-b846-6bd617a87abf">Using Dialog Boxes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bda42841-cc26-44c7-9295-3b3bc818d269">CheckDlgButton</a>
 

 

