---
UID: NF:processthreadsapi.QueueUserAPC
title: QueueUserAPC function (processthreadsapi.h)
description: Adds a user-mode asynchronous procedure call (APC) object to the APC queue of the specified thread. (QueueUserAPC)
helpviewer_keywords: ["QueueUserAPC","QueueUserAPC function","_win32_queueuserapc","base.queueuserapc","processthreadsapi/QueueUserAPC","winbase/QueueUserAPC"]
old-location: base\queueuserapc.htm
tech.root: processthreadsapi
ms.assetid: 5b141372-7c95-4eb2-987b-64fdf7d0783d
ms.date: 12/05/2018
ms.keywords: QueueUserAPC, QueueUserAPC function, _win32_queueuserapc, base.queueuserapc, processthreadsapi/QueueUserAPC, winbase/QueueUserAPC
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueueUserAPC
 - processthreadsapi/QueueUserAPC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
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
---

# QueueUserAPC function

## -description

Adds a user-mode [asynchronous procedure call](/windows/win32/sync/asynchronous-procedure-calls) (APC) object to the APC queue of the specified thread.

## -parameters

### -param pfnAPC [in]

A pointer to the application-supplied APC function to be called when the specified thread performs an alertable wait operation. For more information, see [PAPCFUNC callback function](../winnt/nc-winnt-papcfunc.md).

### -param hThread [in]

A handle to the thread. The handle must have the **THREAD_SET_CONTEXT** access right. For more information, see [Synchronization Object Security and Access Rights](/windows/desktop/Sync/synchronization-object-security-and-access-rights).

### -param dwData [in]

A single value that is passed to the APC function pointed to by the *pfnAPC* parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). **Windows Server 2003 and Windows XP:** There are no error values defined for this function that can be retrieved by calling [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

See [QueueUserAPC2 function](nf-processthreadsapi-queueuserapc2.md) for information on special user-mode APCs.

The APC support provided in the operating system allows an application to queue an APC object to a thread. To ensure successful execution of  functions used by the APC, APCs  should be queued only to   threads in the caller's process.

>[!NOTE]
> Queuing APCs to threads outside the caller's process is not recommended for a number of reasons. DLL rebasing can cause the addresses of functions used by the APC to be incorrect when the functions are executed outside the caller's process. Similarly, if a 64-bit process queues an APC to a 32-bit process or vice versa, addresses will be incorrect and the application will crash. Other factors can prevent successful function execution, even if the address is known.

Each thread has its own APC queue. The queuing of an APC is a request for the thread to call the APC function. The operating system issues a software interrupt to direct the thread to call the APC function.

When a user-mode APC is queued, the thread is not directed to call the APC function unless it is in an alertable state. After the thread is in an alertable state, the thread handles all pending APCs in first in, first out (FIFO) order, and the wait operation returns **WAIT_IO_COMPLETION**. A thread enters an alertable state by using [SleepEx function](../synchapi/nf-synchapi-sleepex.md), [SignalObjectAndWait function](../synchapi/nf-synchapi-signalobjectandwait.md), [WaitForSingleObjectEx function](../synchapi/nf-synchapi-waitforsingleobjectex.md), [WaitForMultipleObjectsEx function](../synchapi/nf-synchapi-waitformultipleobjectsex.md), or [MsgWaitForMultipleObjectsEx function](../winuser/nf-winuser-msgwaitformultipleobjectsex.md).

If an application queues an APC before the thread begins running, the thread begins by calling the APC function. After the thread calls an APC function, it calls the APC functions for all APCs in its APC queue.

It is possible to sleep or wait for an object within the APC. If you perform an alertable wait inside an APC, it will recursively dispatch the APCs. This can cause a stack overflow.

When the thread is terminated using the [ExitThread function](nf-processthreadsapi-exitthread.md) or [TerminateThread function](nf-processthreadsapi-terminatethread.md) function, the APCs in its APC queue are lost. The APC functions are not called.

When the thread is in the process of being terminated, calling QueueUserAPC to add to the thread's APC queue will fail with **(31) ERROR_GEN_FAILURE**.

Note that the [ReadFileEx function](../fileapi/nf-fileapi-readfileex.md), [SetWaitableTimer function](../synchapi/nf-synchapi-setwaitabletimer.md), and [WriteFileEx function](../fileapi/nf-fileapi-writefileex.md) functions are implemented using an APC as the completion notification callback mechanism.

To compile an application that uses this function, define **_WIN32_WINNT** as 0x0400 or later. For more information, see [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers).

## -see-also

- [PAPCFUNC callback function](../winnt/nc-winnt-papcfunc.md)
- [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls)
- [Synchronization Functions](/windows/desktop/Sync/synchronization-functions)
