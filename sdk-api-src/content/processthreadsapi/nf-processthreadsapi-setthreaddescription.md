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

# SetThreadDescription function


## -description


Assigns a description to a thread.


## -parameters




### -param hThread [in]

A handle for the thread for which you want to set the description. The handle must have THREAD_SET_LIMITED_INFORMATION access.


### -param lpThreadDescription [in]

A Unicode string that specifies the description of the thread.


## -returns



If the function succeeds, the return value is the <b>HRESULT</b> that denotes a successful operation.
If the function fails, the return value is an <b>HRESULT</b> that denotes the error.
 




## -remarks



The description of a thread can be set more than once; the most recently set value is used. You can retrieve the description of a thread by calling <a href="https://msdn.microsoft.com/9CFF0A2D-2196-4AE0-8F77-229A8AB7A3E8">GetThreadDescription</a>.


#### Examples

The following example sets the description for the current thread to "simulation_thread".

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = SetThreadDescription(GetCurrentThread(), L"simulation_thread");
if (FAILED(hr))
{
    // Call failed.
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9CFF0A2D-2196-4AE0-8F77-229A8AB7A3E8">GetThreadDescription</a>
 

 

