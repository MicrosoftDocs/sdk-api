---
UID: NF:threadpoollegacyapiset.CreateTimerQueue
title: CreateTimerQueue function (threadpoollegacyapiset.h)
description: Creates a queue for timers.
helpviewer_keywords: ["CreateTimerQueue","CreateTimerQueue function","_win32_createtimerqueue","base.createtimerqueue","threadpoollegacyapiset/CreateTimerQueue","winbase/CreateTimerQueue"]
old-location: base\createtimerqueue.htm
tech.root: backup
ms.assetid: 7d88dc0d-4650-4197-a719-01e2f5ff96df
ms.date: 12/05/2018
ms.keywords: CreateTimerQueue, CreateTimerQueue function, _win32_createtimerqueue, base.createtimerqueue, threadpoollegacyapiset/CreateTimerQueue, winbase/CreateTimerQueue
req.header: threadpoollegacyapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CreateTimerQueue
 - threadpoollegacyapiset/CreateTimerQueue
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
 - API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateTimerQueue
---

# CreateTimerQueue function


## -description

Creates a queue for timers. Timer-queue timers are lightweight objects that enable you to specify a callback function to be called at a specified time.



## -returns

If the function succeeds, the return value is a handle to the timer queue. This handle can be used only in functions that require a handle to a timer queue.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To add a timer to the queue, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a> function. To remove a timer from the queue, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a> function.

When you are finished with the queue of timers, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a> function to delete the timer queue. Any pending timers in the queue are canceled and deleted.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>CreateTimerQueue</b>, see 
<a href="/windows/desktop/Sync/using-timer-queues">Using Timer Queues</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>
