---
UID: NF:processthreadsapi.QueueUserAPC
title: QueueUserAPC function (processthreadsapi.h)
description: Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread.
old-location: base\queueuserapc.htm
tech.root: Sync
ms.assetid: 5b141372-7c95-4eb2-987b-64fdf7d0783d
ms.date: 12/05/2018
ms.keywords: QueueUserAPC, QueueUserAPC function, _win32_queueuserapc, base.queueuserapc, processthreadsapi/QueueUserAPC, winbase/QueueUserAPC
f1_keywords:
- processthreadsapi/QueueUserAPC
dev_langs:
- c++
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-ProcessThreads-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-ProcessThreads-l1-1-1.dll
- API-MS-Win-Core-ProcessThreads-l1-1-2.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
- QueueUserAPC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueueUserAPC function


## -description


Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread.


## -parameters




### -param pfnAPC [in]

A pointer to the application-supplied APC function to be called when the specified thread performs an alertable wait operation. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-papcfunc">APCProc</a>.


### -param hThread [in]

A handle to the thread. The handle must have the <b>THREAD_SET_CONTEXT</b> access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.


### -param dwData [in]

A single value that is passed to the APC function pointed to by the <i>pfnAPC</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>Windows Server 2003 and Windows XP:  </b>There are no error values defined for this function that can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.






## -remarks



The APC support provided in the operating system allows an application to queue an APC object to a thread. To ensure successful execution of  functions used by the APC, APCs  should be queued only to   threads in the caller's process. 

<div class="alert"><b>Note</b>  Queuing APCs to threads outside the caller's process is not recommended for a number of reasons. DLL rebasing can cause the addresses of functions used by the APC to be incorrect when the functions are executed outside the caller's process. Similarly, if a 64-bit process queues an APC to a 32-bit process or vice versa, addresses will be incorrect and the application will crash. Other factors can prevent successful function execution, even if the address is known.  </div>
<div> </div>
Each thread has its own APC queue. The queuing of an APC is a request for the thread to call the APC function. The operating system issues a software interrupt to direct the thread to call the APC function.

When a user-mode APC is queued, the thread is not directed to call the APC function unless it is in an alertable state. After the thread is in an alertable state, the thread handles all pending APCs in first in, first out (FIFO) order, and the wait operation returns <b>WAIT_IO_COMPLETION</b>. A thread enters an alertable state by using 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-signalobjectandwait">SignalObjectAndWait</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> to perform an alertable wait operation.

If an application queues an APC before the thread begins running, the thread begins by calling the APC function. After the thread calls an APC function, it calls the APC functions for all APCs in its APC queue.

It is possible to sleep or wait for an object within the APC. If you perform an alertable wait inside an APC, it will recursively dispatch the APCs. This can cause a stack overflow.

When the thread is terminated using the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a> function, the APCs in its APC queue are lost. The APC functions are not called.

When the thread is in the process of being terminated, calling QueueUserAPC to add to the thread's APC queue will fail with <b>(31) ERROR_GEN_FAILURE</b>.

Note that the <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> functions are implemented using an APC as the completion notification callback mechanism.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-papcfunc">APCProc</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

