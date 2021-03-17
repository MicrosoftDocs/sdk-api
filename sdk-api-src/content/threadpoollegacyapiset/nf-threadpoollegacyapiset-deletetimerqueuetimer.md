---
UID: NF:threadpoollegacyapiset.DeleteTimerQueueTimer
title: DeleteTimerQueueTimer function (threadpoollegacyapiset.h)
description: Removes a timer from the timer queue and optionally waits for currently running timer callback functions to complete before deleting the timer.
helpviewer_keywords: ["DeleteTimerQueueTimer","DeleteTimerQueueTimer function","_win32_deletetimerqueuetimer","base.deletetimerqueuetimer","threadpoollegacyapiset/DeleteTimerQueueTimer","winbase/DeleteTimerQueueTimer"]
old-location: base\deletetimerqueuetimer.htm
tech.root: backup
ms.assetid: d830fa1f-504a-4921-865c-34dbf0256720
ms.date: 12/05/2018
ms.keywords: DeleteTimerQueueTimer, DeleteTimerQueueTimer function, _win32_deletetimerqueuetimer, base.deletetimerqueuetimer, threadpoollegacyapiset/DeleteTimerQueueTimer, winbase/DeleteTimerQueueTimer
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
 - DeleteTimerQueueTimer
 - threadpoollegacyapiset/DeleteTimerQueueTimer
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
 - DeleteTimerQueueTimer
---

# DeleteTimerQueueTimer function


## -description

Removes a timer from the timer queue and optionally waits for currently running timer callback functions to complete before deleting the timer.

## -parameters

### -param TimerQueue [in, optional]

A handle to the timer queue. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function. 




If the timer was created using the default timer queue, this parameter should be <b>NULL</b>.

### -param Timer [in]

A handle to the timer-queue timer. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a> function.

### -param CompletionEvent [in, optional]

A handle to the event object to be signaled when the system has canceled the timer and all callback functions  have completed. This parameter can be <b>NULL</b>. 




If this parameter is <b>INVALID_HANDLE_VALUE</b>, the function waits for any running timer callback functions to complete before returning.

If this parameter is <b>NULL</b>, the function marks the timer for deletion and returns immediately. If the timer has already expired, the timer callback function will run to completion. However, there is no notification sent when the timer callback function has completed. Most callers should not use this option, and should wait for running timer callback functions to complete so they can perform any needed cleanup.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the error code is <b>ERROR_IO_PENDING</b>, it is not necessary to call this function again. For any other error, you should retry the call.

## -remarks

This function cannot be called while the thread is using impersonation. The resulting behavior is undefined.

You can set <i>CompletionEvent</i> to <b>INVALID_HANDLE_VALUE</b> when calling this function from within the timer callback of another timer as long as the callback function is not executed in the timer thread. However, a deadlock may occur if two callback functions attempt a blocking 
<b>DeleteTimerQueueTimer</b> call on each others' timers. Furthermore, you cannot make a blocking deletion call on a timer associated with the callback.

Be careful when making a blocking <b>DeleteTimerQueueTimer</b> call on a persistent thread. If the timer being deleted was created with   <b>WT_EXECUTEINPERSISTENTTHREAD</b>, a deadlock may occur.

If there are outstanding callback functions and  <i>CompletionEvent</i> is <b>NULL</b>, the function will fail and set the error code to <b>ERROR_IO_PENDING</b>. This indicates that there are outstanding callback functions. Those callbacks either will execute or are in the middle of executing. The timer is cleaned up when the callback function is finished executing.

To cancel all timers in a timer queue, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>