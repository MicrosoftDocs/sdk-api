---
UID: NS:winuser.tagCOMBOBOXINFO
title: tagCOMBOBOXINFO
author: windows-sdk-content
description: Contains combo box status information.
old-location: controls\COMBOBOXINFO.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\comboboxinfo.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*LPCOMBOBOXINFO, *PCOMBOBOXINFO, COMBOBOXINFO, COMBOBOXINFO structure [Windows Controls], LPCOMBOBOXINFO, LPCOMBOBOXINFO structure pointer [Windows Controls], PCOMBOBOXINFO, PCOMBOBOXINFO structure pointer [Windows Controls], STATE_SYSTEM_INVISIBLE, STATE_SYSTEM_PRESSED, _win32_COMBOBOXINFO_str, _win32_COMBOBOXINFO_str_cpp, controls.COMBOBOXINFO, controls._win32_COMBOBOXINFO_str, tagCOMBOBOXINFO, winuser/COMBOBOXINFO, winuser/LPCOMBOBOXINFO, winuser/PCOMBOBOXINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: COMBOBOXINFO, *PCOMBOBOXINFO, *LPCOMBOBOXINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - COMBOBOXINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagCOMBOBOXINFO structure


## -description


Contains combo box status information.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The size, in bytes, of the structure. The calling application must set this to sizeof(COMBOBOXINFO). 


### -field rcItem

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the coordinates of the edit box. 


### -field rcButton

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the coordinates of the button that contains the drop-down arrow. 


### -field stateButton

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The combo box button state. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The button exists and is not pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_INVISIBLE"></a><a id="state_system_invisible"></a><dl>
<dt><b>STATE_SYSTEM_INVISIBLE</b></dt>
</dl>
</td>
<td width="60%">
There is no button.

</td>
</tr>
<tr>
<td width="40%"><a id="STATE_SYSTEM_PRESSED"></a><a id="state_system_pressed"></a><dl>
<dt><b>STATE_SYSTEM_PRESSED</b></dt>
</dl>
</td>
<td width="60%">
The button is pressed.

</td>
</tr>
</table>
 


### -field hwndCombo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the combo box. 


### -field hwndItem

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit box. 


### -field hwndList

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the drop-down list. 


## -remarks



The following example code retrieves information about the combo box specified by the window handle.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>COMBOBOXINFO info = { sizeof(COMBOBOXINFO) };
GetComboBoxInfo(hwnd, &amp;info);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f7553df7-4309-49fc-9e4a-da9063e6b042">GetComboBoxInfo</a>
 

 

