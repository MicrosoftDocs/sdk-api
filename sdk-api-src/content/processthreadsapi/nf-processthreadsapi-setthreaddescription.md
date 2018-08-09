---
UID: NF:processthreadsapi.SetThreadDescription
title: SetThreadDescription function
author: windows-sdk-content
description: Assigns a description to a thread.
old-location: base\setthreaddescription.htm
old-project: procthread
ms.assetid: 0C17C60A-8DC9-4DB1-A3ED-5AFEBE598CBB
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetThreadDescription, SetThreadDescription function, base.setthreaddescription, processthreadsapi/SetThreadDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - KernelBase.dll
 - Api-ms-win-core-processthreads-l1-1-3.dll
api_name:
 - SetThreadDescription
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
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
 

 

