---
UID: NF:threadpoollegacyapiset.CreateTimerQueue
title: CreateTimerQueue function
author: windows-sdk-content
description: Creates a queue for timers.
old-location: base\createtimerqueue.htm
tech.root: Sync
ms.assetid: 7d88dc0d-4650-4197-a719-01e2f5ff96df
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateTimerQueue, CreateTimerQueue function, _win32_createtimerqueue, base.createtimerqueue, threadpoollegacyapiset/CreateTimerQueue, winbase/CreateTimerQueue
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
 - CreateTimerQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateTimerQueue function


## -description


Creates a queue for timers. Timer-queue timers are lightweight objects that enable you to specify a callback function to be called at a specified time.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the timer queue. This handle can be used only in functions that require a handle to a timer queue.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To add a timer to the queue, call the 
<a href="https://msdn.microsoft.com/dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844">CreateTimerQueueTimer</a> function. To remove a timer from the queue, call the 
<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a> function.

When you are finished with the queue of timers, call the 
<a href="https://msdn.microsoft.com/782f85df-b176-4bff-a048-d7fcdd8196b0">DeleteTimerQueueEx</a> function to delete the timer queue. Any pending timers in the queue are canceled and deleted.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>CreateTimerQueue</b>, see 
<a href="https://msdn.microsoft.com/779156fe-f825-452b-acbe-e2cb189e24d2">Using Timer Queues</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844">CreateTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/782f85df-b176-4bff-a048-d7fcdd8196b0">DeleteTimerQueueEx</a>



<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>



<a href="https://msdn.microsoft.com/ee85a6c3-3a1d-4f94-9112-cb8247b2a189">Timer Queues</a>
 

 

