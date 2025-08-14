---
UID: NF:threadpoollegacyapiset.DeleteTimerQueue
tech.root: backup
title: DeleteTimerQueue
ms.date: 06/02/2021
targetos: Windows
description: Deletes a timer queue. Any pending timers in the queue are canceled and deleted. (DeleteTimerQueue)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.lib
req.header: threadpoollegacyapiset.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-threadpool-legacy-l1-1-0.dll
 - Kernel32.dll
api_name:
 - DeleteTimerQueue
f1_keywords:
 - DeleteTimerQueue
 - threadpoollegacyapiset/DeleteTimerQueue
dev_langs:
 - c++
---

## -description

Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
<div class="alert"><b>Note</b>  This function is obsolete and has been replaced by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a> function.</div><div> </div>


## -parameters

### -param TimerQueue

A handle to the timer queue. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function.


## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


## -remarks

<b>DeleteTimerQueue</b> does not wait for all callback functions associated with the timer to complete.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>DeleteTimerQueue</b>, see 
<a href="/windows/desktop/Sync/using-timer-queues">Using Timer Queues</a>.

<div class="code"></div>

## -see-also


<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>

