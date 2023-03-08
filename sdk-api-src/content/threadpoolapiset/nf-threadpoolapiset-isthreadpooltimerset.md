---
UID: NF:threadpoolapiset.IsThreadpoolTimerSet
title: IsThreadpoolTimerSet function (threadpoolapiset.h)
description: Determines whether the specified timer object is currently set.
helpviewer_keywords: ["IsThreadpoolTimerSet","IsThreadpoolTimerSet function","base.isthreadpooltimerset","threadpoolapiset/IsThreadpoolTimerSet","winbase/IsThreadpoolTimerSet"]
old-location: base\isthreadpooltimerset.htm
tech.root: backup
ms.assetid: f9dee0aa-6310-4218-b207-72a24c5019e2
ms.date: 12/05/2018
ms.keywords: IsThreadpoolTimerSet, IsThreadpoolTimerSet function, base.isthreadpooltimerset, threadpoolapiset/IsThreadpoolTimerSet, winbase/IsThreadpoolTimerSet
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsThreadpoolTimerSet
 - threadpoolapiset/IsThreadpoolTimerSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - IsThreadpoolTimerSet
---

# IsThreadpoolTimerSet function


## -description

Determines whether the specified timer object is currently set.

## -parameters

### -param pti [in, out]

A pointer to a <b>TP_TIMER</b> structure that defines the timer object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a> function returns this pointer.

## -returns

The return value is TRUE if the timer is set; otherwise, the return value is FALSE.

## -remarks

A timer is considered to be set if the most recent call to [SetThreadpoolTimer](nf-threadpoolapiset-setthreadpooltimer.md)
or [SetThreadpoolTimerEx function](nf-threadpoolapiset-setthreadpooltimerex.md) passed a non-null value for <i>pftDueTime</i>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a>