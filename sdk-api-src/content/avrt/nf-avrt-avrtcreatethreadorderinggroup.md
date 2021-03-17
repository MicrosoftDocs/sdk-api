---
UID: NF:avrt.AvRtCreateThreadOrderingGroup
title: AvRtCreateThreadOrderingGroup function (avrt.h)
description: Creates a thread ordering group.
helpviewer_keywords: ["AvRtCreateThreadOrderingGroup","AvRtCreateThreadOrderingGroup function","avrt/AvRtCreateThreadOrderingGroup","base.avrtcreatethreadorderinggroup"]
old-location: base\avrtcreatethreadorderinggroup.htm
tech.root: backup
ms.assetid: c334a861-7dd6-4fc9-90ce-5923d053d325
ms.date: 12/05/2018
ms.keywords: AvRtCreateThreadOrderingGroup, AvRtCreateThreadOrderingGroup function, avrt/AvRtCreateThreadOrderingGroup, base.avrtcreatethreadorderinggroup
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
 - AvRtCreateThreadOrderingGroup
 - avrt/AvRtCreateThreadOrderingGroup
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
 - AvRtCreateThreadOrderingGroup
---

# AvRtCreateThreadOrderingGroup function


## -description

Creates a thread ordering group.

To prevent the server thread for the thread ordering group from being starved if higher priority client threads are running, use the <a href="/windows/desktop/api/avrt/nf-avrt-avrtcreatethreadorderinggroupexa">AvRtCreateThreadOrderingGroupEx</a> function.

## -parameters

### -param Context [out]

A pointer to a context handle.

### -param Period [in]

A pointer to a value, in 100-nanosecond increments, that specifies the period for the thread ordering group. Each thread in the thread ordering group runs one time during this period. If all threads complete their execution before a period ends, all threads wait until the remainder of the period elapses before any are executed again.

The possible values for this parameter depend on the platform, but this parameter can be as low as 500 microseconds or as high as 0x1FFFFFFFFFFFFFFF. If this parameter is less than 500 microseconds, then it is set to 500 microseconds. If this parameter is greater than the maximum, then it is set to 0x1FFFFFFFFFFFFFFF.

### -param ThreadOrderingGuid [in, out]

A pointer to the unique identifier for the thread ordering group to be created. If this value is not unique to the thread ordering service, the function fails.

If the identifier is GUID_NULL on input, the thread ordering service generates and returns a unique identifier.

### -param Timeout [in, optional]

A pointer to a time-out value. All threads within the group should complete their execution within <i>Period</i> plus <i>Timeout</i>.

If a thread fails to complete its processing within the period plus this time-out interval, it is removed from the thread ordering group. If the parent fails to complete its processing within the period plus the time-out interval, the thread ordering group is destroyed.

The possible values for this parameter depend on the platform, but can be as low as 500 microseconds or as high as 0x1FFFFFFFFFFFFFFF. If this parameter is less than 500 microseconds, then it is set to 500 microseconds. If this parameter is greater than the maximum, then it is set to 0x1FFFFFFFFFFFFFFF.

If this parameter is <b>NULL</b> or 0, the default is five times the value of <i>Period</i>.

If this parameter is THREAD_ORDER_GROUP_INFINITE_TIMEOUT, the group is created with an infinite time-out interval. This can be useful for debugging purposes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If a thread ordering group with the specified identifier already exists, the function fails and sets the last error to ERROR_ALREADY_EXISTS.

## -remarks

The calling thread is considered to be the parent thread. Each thread ordering group has one parent thread. Each parent thread can have zero or more predecessor threads and zero or more successor threads. A client thread can join a thread ordering group and specify whether it is a predecessor or successor using the <a href="/windows/desktop/api/avrt/nf-avrt-avrtjointhreadorderinggroup">AvRtJoinThreadOrderingGroup</a> function.

The parent thread encloses the code to be executed during each period within a loop that is controlled by the <a href="/windows/desktop/api/avrt/nf-avrt-avrtwaitonthreadorderinggroup">AvRtWaitOnThreadOrderingGroup</a> function.

To delete the thread ordering group, call the <a href="/windows/desktop/api/avrt/nf-avrt-avrtdeletethreadorderinggroup">AvRtDeleteThreadOrderingGroup</a> function.

A thread can create more than one thread ordering group and join more than one thread ordering group. However, a thread cannot join the same thread ordering group more than one time.


#### Examples

The following snippet creates a thread ordering group.


```cpp
#include <windows.h>
#include <avrt.h>
#include <stdio.h>

#pragma comment(lib, "Avrt.lib")

#define _100NS_IN_1MS 10000

int main( void )
{
    HANDLE hContext = NULL;
    LARGE_INTEGER period, timeout;
    GUID guid = { 0 };
    BOOL bRes;

    period.QuadPart = Int32x32To64(_100NS_IN_1MS, 1000);   // 1 second
    timeout.QuadPart = Int32x32To64(_100NS_IN_1MS, 10000); // 10 seconds

    bRes = AvRtCreateThreadOrderingGroup( 
            &hContext,
            &period,
            &guid,
            &timeout );

    if( bRes != TRUE )
    {
        printf("Error creating group (%d)\n", GetLastError());
            return 1;
    }

    return 0;
}

```

## -see-also

<a href="/windows/desktop/ProcThread/thread-ordering-service">Thread Ordering Service</a>