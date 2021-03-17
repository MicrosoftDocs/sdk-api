---
UID: NF:threadpoollegacyapiset.ChangeTimerQueueTimer
title: ChangeTimerQueueTimer function (threadpoollegacyapiset.h)
description: Updates a timer-queue timer that was created by the CreateTimerQueueTimer function.
helpviewer_keywords: ["ChangeTimerQueueTimer","ChangeTimerQueueTimer function","_win32_changetimerqueuetimer","base.changetimerqueuetimer","threadpoollegacyapiset/ChangeTimerQueueTimer","winbase/ChangeTimerQueueTimer"]
old-location: base\changetimerqueuetimer.htm
tech.root: backup
ms.assetid: 251a9a18-f98c-4334-a333-3c73638d7d93
ms.date: 12/05/2018
ms.keywords: ChangeTimerQueueTimer, ChangeTimerQueueTimer function, _win32_changetimerqueuetimer, base.changetimerqueuetimer, threadpoollegacyapiset/ChangeTimerQueueTimer, winbase/ChangeTimerQueueTimer
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
 - ChangeTimerQueueTimer
 - threadpoollegacyapiset/ChangeTimerQueueTimer
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
 - ChangeTimerQueueTimer
---

# ChangeTimerQueueTimer function


## -description

Updates a timer-queue timer that was created by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a> function.

## -parameters

### -param TimerQueue [in, optional]

A handle to the timer queue. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function. 




If this parameter is <b>NULL</b>, the timer is associated with the default timer queue.

### -param Timer [in, out]

A handle to the timer-queue timer. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a> function.

### -param DueTime [in]

The time after which the timer should expire, in milliseconds.

### -param Period [in]

The period of the timer, in milliseconds. If this parameter is zero, the timer is signaled once. If this parameter is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled using the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a> function or reset using 
<b>ChangeTimerQueueTimer</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function cannot be called while the thread is using impersonation. The resulting behavior is undefined.

You can call 
<b>ChangeTimerQueueTimer</b> in a timer callback.

If you call 
<b>ChangeTimerQueueTimer</b> on a one-shot timer (its period is zero) that has already expired, the timer is not updated.

Do not call 
<b>ChangeTimerQueueTimer</b> after calling 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a> on a handle.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer">CreateTimerQueueTimer</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>