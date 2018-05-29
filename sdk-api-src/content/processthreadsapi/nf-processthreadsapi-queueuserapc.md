---
UID: NF:processthreadsapi.QueueUserAPC
title: QueueUserAPC function
author: windows-sdk-content
description: Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread.
old-location: base\queueuserapc.htm
old-project: Sync
ms.assetid: 5b141372-7c95-4eb2-987b-64fdf7d0783d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: QueueUserAPC, QueueUserAPC function, _win32_queueuserapc, base.queueuserapc, processthreadsapi/QueueUserAPC, winbase/QueueUserAPC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-1.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l1-1-0.dll
-	API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
-	QueueUserAPC
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# QueueUserAPC function


## -description


Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread.


## -parameters




### -param pfnAPC [in]

A pointer to the application-supplied APC function to be called when the specified thread performs an alertable wait operation. For more information, see 
<a href="https://msdn.microsoft.com/8d52ad73-0172-4d1d-b625-39629e7f5823">APCProc</a>.


### -param hThread [in]

A handle to the thread. The handle must have the <b>THREAD_SET_CONTEXT</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param dwData [in]

A single value that is passed to the APC function pointed to by the <i>pfnAPC</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>Windows Server 2003 and Windows XP:  </b>There are no error values defined for this function that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.






## -remarks



The APC support provided in the operating system allows an application to queue an APC object to a thread. To ensure successful execution of  functions used by the APC, APCs  should be queued only to   threads in the caller's process. 

<div class="alert"><b>Note</b>  Queuing APCs to threads outside the caller's process is not recommended for a number of reasons. DLL rebasing can cause the addresses of functions used by the APC to be incorrect when the functions are executed outside the caller's process. Similarly, if a 64-bit process queues an APC to a 32-bit process or vice versa, addresses will be incorrect and the application will crash. Other factors can prevent successful function execution, even if the address is known.  </div>
<div> </div>
Each thread has its own APC queue. The queuing of an APC is a request for the thread to call the APC function. The operating system issues a software interrupt to direct the thread to call the APC function.

When a user-mode APC is queued, the thread is not directed to call the APC function unless it is in an alertable state. After the thread is in an alertable state, the thread handles all pending APCs in first in, first out (FIFO) order, and the wait operation returns <b>WAIT_IO_COMPLETION</b>. A thread enters an alertable state by using 
<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>, 
<a href="https://msdn.microsoft.com/2b1ce22b-8edb-4685-99f4-4fc38eec202a">SignalObjectAndWait</a>, 
<a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>, 
<a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>, or 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a> to perform an alertable wait operation.

If an application queues an APC before the thread begins running, the thread begins by calling the APC function. After the thread calls an APC function, it calls the APC functions for all APCs in its APC queue.

It is possible to sleep or wait for an object within the APC. If you perform an alertable wait inside an APC, it will recursively dispatch the APCs. This can cause a stack overflow.

When the thread is terminated using the 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> or 
<a href="https://msdn.microsoft.com/ae1ad0f3-67df-4573-af22-7086f0470361">TerminateThread</a> function, the APCs in its APC queue are lost. The APC functions are not called.

When the thread is in the process of being terminated, calling QueueUserAPC to add to the thread's APC queue will fail with <b>(31) ERROR_GEN_FAILURE</b>.

Note that the <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>, 
<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>, and <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> functions are implemented using an APC as the completion notification callback mechanism.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8d52ad73-0172-4d1d-b625-39629e7f5823">APCProc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540625">Asynchronous Procedure Calls</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

