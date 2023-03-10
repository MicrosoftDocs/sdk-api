---
UID: NF:threadpoollegacyapiset.DeleteTimerQueueEx
title: DeleteTimerQueueEx function (threadpoollegacyapiset.h)
description: Deletes a timer queue. Any pending timers in the queue are canceled and deleted. (DeleteTimerQueueEx)
helpviewer_keywords: ["DeleteTimerQueueEx","DeleteTimerQueueEx function","_win32_deletetimerqueueex","base.deletetimerqueueex","threadpoollegacyapiset/DeleteTimerQueueEx","winbase/DeleteTimerQueueEx"]
old-location: base\deletetimerqueueex.htm
tech.root: backup
ms.assetid: 782f85df-b176-4bff-a048-d7fcdd8196b0
ms.date: 12/05/2018
ms.keywords: DeleteTimerQueueEx, DeleteTimerQueueEx function, _win32_deletetimerqueueex, base.deletetimerqueueex, threadpoollegacyapiset/DeleteTimerQueueEx, winbase/DeleteTimerQueueEx
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
 - DeleteTimerQueueEx
 - threadpoollegacyapiset/DeleteTimerQueueEx
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
 - DeleteTimerQueueEx
---

# DeleteTimerQueueEx function


## -description

Deletes a timer queue. Any pending timers in the queue are canceled and deleted.

## -parameters

### -param TimerQueue [in]

A handle to the timer queue. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function.

### -param CompletionEvent [in, optional]

A handle to the event object to be signaled when the function is successful and all callback functions have completed. This parameter can be <b>NULL</b>. 




If this parameter is <b>INVALID_HANDLE_VALUE</b>, the function waits for all callback functions to complete before returning.

If this parameter is <b>NULL</b>, the function marks the timer for deletion and returns immediately. However, most callers should wait for the callback function to complete so they can perform any needed cleanup.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not make blocking calls to 
<b>DeleteTimerQueueEx</b> from within a timer callback.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>
