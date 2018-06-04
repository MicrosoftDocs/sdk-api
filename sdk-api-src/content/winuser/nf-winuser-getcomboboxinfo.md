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
 

 

