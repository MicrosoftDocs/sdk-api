---
UID: NF:threadpoollegacyapiset.ChangeTimerQueueTimer
title: ChangeTimerQueueTimer function (threadpoollegacyapiset.h)
author: windows-sdk-content
description: Updates a timer-queue timer that was created by the CreateTimerQueueTimer function.
old-location: base\changetimerqueuetimer.htm
tech.root: Sync
ms.assetid: 251a9a18-f98c-4334-a333-3c73638d7d93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ChangeTimerQueueTimer, ChangeTimerQueueTimer function, _win32_changetimerqueuetimer, base.changetimerqueuetimer, threadpoollegacyapiset/ChangeTimerQueueTimer, winbase/ChangeTimerQueueTimer
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ChangeTimerQueueTimer function


## -description


Updates a timer-queue timer that was created by the 
<a href="https://msdn.microsoft.com/dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844">CreateTimerQueueTimer</a> function.


## -parameters




### -param TimerQueue [in, optional]

A handle to the timer queue. This handle is returned by the 
<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a> function. 




If this parameter is <b>NULL</b>, the timer is associated with the default timer queue.


### -param Timer [in, out]

A handle to the timer-queue timer. This handle is returned by the 
<a href="https://msdn.microsoft.com/dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844">CreateTimerQueueTimer</a> function.


### -param DueTime [in]

The time after which the timer should expire, in milliseconds.


### -param Period [in]

The period of the timer, in milliseconds. If this parameter is zero, the timer is signaled once. If this parameter is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled using the 
<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a> function or reset using 
<b>ChangeTimerQueueTimer</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function cannot be called while the thread is using impersonation. The resulting behavior is undefined.

You can call 
<b>ChangeTimerQueueTimer</b> in a timer callback.

If you call 
<b>ChangeTimerQueueTimer</b> on a one-shot timer (its period is zero) that has already expired, the timer is not updated.

Do not call 
<b>ChangeTimerQueueTimer</b> after calling 
<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a> on a handle.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a>



<a href="https://msdn.microsoft.com/dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844">CreateTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>



<a href="https://msdn.microsoft.com/ee85a6c3-3a1d-4f94-9112-cb8247b2a189">Timer Queues</a>
 

 

