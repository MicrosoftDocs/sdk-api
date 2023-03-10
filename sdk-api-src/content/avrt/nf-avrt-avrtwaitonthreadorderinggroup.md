---
UID: NF:avrt.AvRtWaitOnThreadOrderingGroup
title: AvRtWaitOnThreadOrderingGroup function (avrt.h)
description: Enables client threads of a thread ordering group to wait until they should execute.
helpviewer_keywords: ["AvRtWaitOnThreadOrderingGroup","AvRtWaitOnThreadOrderingGroup function","avrt/AvRtWaitOnThreadOrderingGroup","base.avrtwaitonthreadorderinggroup"]
old-location: base\avrtwaitonthreadorderinggroup.htm
tech.root: backup
ms.assetid: 11318ce3-d938-4bb5-adb1-28dd15e8cd80
ms.date: 12/05/2018
ms.keywords: AvRtWaitOnThreadOrderingGroup, AvRtWaitOnThreadOrderingGroup function, avrt/AvRtWaitOnThreadOrderingGroup, base.avrtwaitonthreadorderinggroup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AvRtWaitOnThreadOrderingGroup
 - avrt/AvRtWaitOnThreadOrderingGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtWaitOnThreadOrderingGroup
---

# AvRtWaitOnThreadOrderingGroup function


## -description

Enables client threads of a thread ordering group to wait until they should execute.

## -parameters

### -param Context [in]

A context handle. This handle is returned by the <a href="/windows/desktop/api/avrt/nf-avrt-avrtcreatethreadorderinggroup">AvRtCreateThreadOrderingGroup</a> or <a href="/windows/desktop/api/avrt/nf-avrt-avrtjointhreadorderinggroup">AvRtJoinThreadOrderingGroup</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When this function returns, the thread should complete its processing for the period and then call the function again.

If the thread fails to complete its processing during the time-out interval specified by the parent thread when creating the group, it is deleted from the thread ordering group. Therefore, when the thread finishes its processing loop, the next call to <b>AvRtWaitOnThreadOrderingGroup</b> fails and the last error code is set to ERROR_ACCESS_DENIED.

If the thread ordering group is deleted during the wait, this function eventually times out and return ERROR_ACCESS_DENIED.


#### Examples


```cpp
#include <windows.h>
#include <avrt.h>
#include <stdio.h>

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

```

## -see-also

<a href="/windows/desktop/ProcThread/thread-ordering-service">Thread Ordering Service</a>