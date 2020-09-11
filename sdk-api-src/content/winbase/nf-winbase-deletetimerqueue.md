---
UID: NF:winbase.DeleteTimerQueue
title: DeleteTimerQueue function (winbase.h)
description: Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
helpviewer_keywords: ["DeleteTimerQueue","DeleteTimerQueue function","_win32_deletetimerqueue","base.deletetimerqueue","winbase/DeleteTimerQueue"]
old-location: base\deletetimerqueue.htm
tech.root: backup
ms.assetid: 29dde4ec-1c95-4417-a8bf-ab9bd56e3f6f
ms.date: 12/05/2018
ms.keywords: DeleteTimerQueue, DeleteTimerQueue function, _win32_deletetimerqueue, base.deletetimerqueue, winbase/DeleteTimerQueue
req.header: winbase.h
req.include-header: Windows.h
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
 - DeleteTimerQueue
 - winbase/DeleteTimerQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DeleteTimerQueue
---

# DeleteTimerQueue function


## -description

Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
<div class="alert"><b>Note</b>  This function is obsolete and has been replaced by the 
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a> function.</div><div> </div>

## -parameters

### -param TimerQueue [in]

A handle to the timer queue. This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>DeleteTimerQueue</b> does not wait for all callback functions associated with the timer to complete.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>DeleteTimerQueue</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/using-timer-queues">Using Timer Queues</a>.

<div class="code"></div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/timer-queues">Timer Queues</a>

