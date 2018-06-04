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

# AvRtDeleteThreadOrderingGroup function


## -description


Deletes the specified thread ordering group created by the caller. It cleans up  resources for the thread ordering group, including the context information, and returns.


## -parameters




### -param Context [in]

A context handle. This handle is returned by the <a href="https://msdn.microsoft.com/c334a861-7dd6-4fc9-90ce-5923d053d325">AvRtCreateThreadOrderingGroup</a> function when creating the group.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can only be called successfully by the parent thread for the thread ordering group. If a thread other than the parent thread calls this function, the function fails with a last error code of ERROR_INVALID_FUNCTION.

If the parent thread times out and attempts to call this function, the function fails with a last error code of ERROR_INVALID_PARAMETER.


#### Examples

The following code deletes a thread ordering group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;avrt.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "Avrt.lib")

HANDLE Context;

int main( void )
{
    if(!AvRtDeleteThreadOrderingGroup(Context))
    {
        printf("Error deleting group (%d)\n", GetLastError());
        return 1;
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 

