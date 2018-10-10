---
UID: NF:winbase.DeleteTimerQueue
title: DeleteTimerQueue function
author: windows-sdk-content
description: Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
old-location: base\deletetimerqueue.htm
tech.root: Sync
ms.assetid: 29dde4ec-1c95-4417-a8bf-ab9bd56e3f6f
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: DeleteTimerQueue, DeleteTimerQueue function, _win32_deletetimerqueue, base.deletetimerqueue, winbase/DeleteTimerQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DeleteTimerQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteTimerQueue function


## -description


Deletes a timer queue. Any pending timers in the queue are canceled and deleted.
<div class="alert"><b>Note</b>  This function is obsolete and has been replaced by the 
<a href="https://msdn.microsoft.com/782f85df-b176-4bff-a048-d7fcdd8196b0">DeleteTimerQueueEx</a> function.</div><div> </div>

## -parameters




### -param TimerQueue [in]

A handle to the timer queue. This handle is returned by the 
<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>DeleteTimerQueue</b> does not wait for all callback functions associated with the timer to complete.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>DeleteTimerQueue</b>, see 
<a href="https://msdn.microsoft.com/779156fe-f825-452b-acbe-e2cb189e24d2">Using Timer Queues</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a>



<a href="https://msdn.microsoft.com/782f85df-b176-4bff-a048-d7fcdd8196b0">DeleteTimerQueueEx</a>



<a href="https://msdn.microsoft.com/d830fa1f-504a-4921-865c-34dbf0256720">DeleteTimerQueueTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>



<a href="https://msdn.microsoft.com/ee85a6c3-3a1d-4f94-9112-cb8247b2a189">Timer Queues</a>
 

 

