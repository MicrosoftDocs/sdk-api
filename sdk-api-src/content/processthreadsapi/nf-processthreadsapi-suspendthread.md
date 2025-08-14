---
UID: NF:processthreadsapi.SuspendThread
title: SuspendThread function (processthreadsapi.h)
description: Suspends the specified thread.
helpviewer_keywords: ["SuspendThread","SuspendThread function","_win32_suspendthread","base.suspendthread","processthreadsapi/SuspendThread","winbase/SuspendThread"]
old-location: base\suspendthread.htm
tech.root: processthreadsapi
ms.assetid: 1332abcb-3356-4890-a03c-843358c1a3ce
ms.date: 12/05/2018
ms.keywords: SuspendThread, SuspendThread function, _win32_suspendthread, base.suspendthread, processthreadsapi/SuspendThread, winbase/SuspendThread
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SuspendThread
 - processthreadsapi/SuspendThread
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
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SuspendThread
---

# SuspendThread function

## -description

Suspends the specified thread.

> [!NOTE]
> A 64-bit application can suspend a WOW64 thread thread using the [Wow64SuspendThread function](../wow64apiset/nf-wow64apiset-wow64suspendthread.md).

## -parameters

### -param hThread [in]

A handle to the thread that is to be suspended.

The handle must have the <b>THREAD_SUSPEND_RESUME</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is the thread's previous suspend count; otherwise, it is <code>(DWORD) -1</code>. To get extended error information, use the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

If the function succeeds, execution of the specified thread is suspended and the thread's suspend count is incremented. Suspending a thread causes the thread to stop executing user-mode (application) code.

This function is primarily designed for use by debuggers. It is not intended to be used for thread synchronization. Calling 
<b>SuspendThread</b> on a thread that owns a synchronization object, such as a mutex or critical section, can lead to a deadlock if the calling thread tries to obtain a synchronization object owned by a suspended thread. To avoid this situation, a thread within an application that is not a debugger should signal the other thread to suspend itself. The target thread must be designed to watch for this signal and respond appropriately.

Each thread has a suspend count (with a maximum value of <b>MAXIMUM_SUSPEND_COUNT</b>). If the suspend count is greater than zero, the thread is suspended; otherwise, the thread is not suspended and is eligible for execution. Calling 
<b>SuspendThread</b> causes the target thread's suspend count to be incremented. Attempting to increment past the maximum suspend count causes an error without incrementing the count.

The 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a> function decrements the suspend count of a suspended thread.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a>



<a href="/windows/desktop/ProcThread/suspending-thread-execution">Suspending Thread Execution</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>