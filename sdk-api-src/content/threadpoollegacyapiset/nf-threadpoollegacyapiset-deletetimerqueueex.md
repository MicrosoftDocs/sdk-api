---
UID: NF:threadpoollegacyapiset.DeleteTimerQueueEx
title: DeleteTimerQueueEx function
author: windows-sdk-content
description: Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
old-location: base\deletetimerqueueex.htm
tech.root: Sync
ms.assetid: 782f85df-b176-4bff-a048-d7fcdd8196b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteTimerQueueEx, DeleteTimerQueueEx function, _win32_deletetimerqueueex, base.deletetimerqueueex, threadpoollegacyapiset/DeleteTimerQueueEx, winbase/DeleteTimerQueueEx
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
 - DeleteTimerQueueEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteTimerQueueEx function


## -description


Deletes a timer queue. Any pending timers in the queue are canceled and deleted.


## -parameters




### -param TimerQueue [in]

A handle to the timer queue. This handle is returned by the 
<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a> function.


### -param CompletionEvent [in, optional]

A handle to the event object to be signaled when the function is successful and all callback functions have completed. This parameter can be <b>NULL</b>. 




If this parameter is <b>INVALID_HANDLE_VALUE</b>, the function waits for all callback functions to complete before returning.

If this parameter is <b>NULL</b>, the function marks the timer for deletion and returns immediately. However, most callers should wait for the callback function to complete so they can perform any needed cleanup.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not make blocking calls to 
<b>DeleteTimerQueueEx</b> from within a timer callback.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a>



<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>



<a href="https://msdn.microsoft.com/ee85a6c3-3a1d-4f94-9112-cb8247b2a189">Timer Queues</a>
 

 

