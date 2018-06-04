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

# GetThreadDescription function


## -description


Retrieves the description that was assigned to a thread by calling <a href="https://msdn.microsoft.com/0C17C60A-8DC9-4DB1-A3ED-5AFEBE598CBB">SetThreadDescription</a>.


## -parameters




### -param hThread [in]

A handle to the thread for which to retrieve the description. The handle must have THREAD_QUERY_LIMITED_INFORMATION access.


### -param ppszThreadDescription

TBD




#### - threadDescription [out]

A Unicode string that contains the description of the thread.


## -returns



If the function succeeds, the return value is the <b>HRESULT</b> that denotes a successful operation.
If the function fails, the return value is an <b>HRESULT</b> that denotes the error.





## -remarks



The description for a thread can change at any time. For example, a different thread can change the description of a thread of interest while you try to retrieve that description.

Thread descriptions do not need to be unique.

To free the memory for the thread description, call the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> method.


#### Examples

The following example gets the description for a thread,  prints the description, and then frees the memory for the description.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = GetThreadDescription(ThreadHandle, &amp;data);
if (SUCCEEDED(hr))
{   
    wprintf(“%ls\m”, data);
    LocalFree(data);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/0C17C60A-8DC9-4DB1-A3ED-5AFEBE598CBB">SetThreadDescription</a>
 

 

