---
UID: NF:winuser.GetComboBoxInfo
title: GetComboBoxInfo function
author: windows-sdk-content
description: Retrieves information about the specified combo box.
old-location: controls\GetComboBoxInfo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxfunctions\getcomboboxinfo.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetComboBoxInfo, GetComboBoxInfo function [Windows Controls], _win32_GetComboBoxInfo, _win32_GetComboBoxInfo_cpp, controls.GetComboBoxInfo, controls._win32_GetComboBoxInfo, winuser/GetComboBoxInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
-	GetComboBoxInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetComboBoxInfo function


## -description


Retrieves information about the specified combo box.


## -parameters




### -param hwndCombo [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the combo box. 


### -param pcbi [out]

Type: <b>PCOMBOBOXINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/8b91ce94-cf26-44a4-b814-c0735ff7ff9b">COMBOBOXINFO</a> structure that receives the information. You must set <b>COMBOBOXINFO.cbSize</b> before calling this function. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/3239dfa8-7301-48e3-ba8e-29c5d5f43b39">CB_GETCOMBOBOXINFO</a> message is equivalent to this function.


#### Examples

The following example code retrieves information about the combo box specified by the window handle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
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




<a href="https://msdn.microsoft.com/3239dfa8-7301-48e3-ba8e-29c5d5f43b39">CB_GETCOMBOBOXINFO</a>



<a href="https://msdn.microsoft.com/8b91ce94-cf26-44a4-b814-c0735ff7ff9b">COMBOBOXINFO</a>



<a href="https://msdn.microsoft.com/e54f216f-5b18-4203-a876-019048ba369f">GetListBoxInfo</a>



<b>Reference</b>
 

 

