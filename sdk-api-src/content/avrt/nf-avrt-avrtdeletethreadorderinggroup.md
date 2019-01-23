---
UID: NF:avrt.AvRtDeleteThreadOrderingGroup
title: AvRtDeleteThreadOrderingGroup function
author: windows-sdk-content
description: Deletes the specified thread ordering group created by the caller. It cleans up resources for the thread ordering group, including the context information, and returns.
old-location: base\avrtdeletethreadorderinggroup.htm
tech.root: procthread
ms.assetid: fa881a0f-3087-4605-9c42-880f6694c018
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AvRtDeleteThreadOrderingGroup, AvRtDeleteThreadOrderingGroup function, avrt/AvRtDeleteThreadOrderingGroup, base.avrtdeletethreadorderinggroup
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
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtDeleteThreadOrderingGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp
#include <windows.h>
#include <avrt.h>
#include <stdio.h>

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

```





## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 

