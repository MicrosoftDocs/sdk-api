---
UID: NF:avrt.AvRtWaitOnThreadOrderingGroup
title: AvRtWaitOnThreadOrderingGroup function
author: windows-sdk-content
description: Enables client threads of a thread ordering group to wait until they should execute.
old-location: base\avrtwaitonthreadorderinggroup.htm
old-project: ProcThread
ms.assetid: 11318ce3-d938-4bb5-adb1-28dd15e8cd80
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: AvRtWaitOnThreadOrderingGroup, AvRtWaitOnThreadOrderingGroup function, avrt/AvRtWaitOnThreadOrderingGroup, base.avrtwaitonthreadorderinggroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: AVRF_HEAP_ALLOCATION, *PAVRF_HEAP_ALLOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtWaitOnThreadOrderingGroup
product: Windows
targetos: Windows
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
---

# AvRtWaitOnThreadOrderingGroup function


## -description


Enables client threads of a thread ordering group to wait until they should execute.


## -parameters




### -param Context [in]

A context handle. This handle is returned by the <a href="https://msdn.microsoft.com/c334a861-7dd6-4fc9-90ce-5923d053d325">AvRtCreateThreadOrderingGroup</a> or <a href="https://msdn.microsoft.com/76e70f91-750e-49c8-8ddf-e8eddd150aa4">AvRtJoinThreadOrderingGroup</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When this function returns, the thread should complete its processing for the period and then call the function again.

If the thread fails to complete its processing during the time-out interval specified by the parent thread when creating the group, it is deleted from the thread ordering group. Therefore, when the thread finishes its processing loop, the next call to <b>AvRtWaitOnThreadOrderingGroup</b> fails and the last error code is set to ERROR_ACCESS_DENIED.

If the thread ordering group is deleted during the wait, this function eventually times out and return ERROR_ACCESS_DENIED.


#### Examples

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
    while(AvRtWaitOnThreadOrderingGroup(Context))
    {
        // Complete task for this period.
    }

return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 

