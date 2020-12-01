---
UID: NF:winbase.Wow64SuspendThread
title: Wow64SuspendThread function (winbase.h)
description: Suspends the specified WOW64 thread.
helpviewer_keywords: ["Wow64SuspendThread","Wow64SuspendThread function","base.wow64suspendthread","winbase/Wow64SuspendThread"]
old-location: base\wow64suspendthread.htm
tech.root: backup
ms.assetid: d976675a-5400-41ac-a11d-c39a1b2dd50d
ms.date: 12/05/2018
ms.keywords: Wow64SuspendThread, Wow64SuspendThread function, base.wow64suspendthread, winbase/Wow64SuspendThread
f1_keywords:
- winbase/Wow64SuspendThread
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Wow64SuspendThread
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Wow64SuspendThread function


## -description


Suspends the specified WOW64 thread.


## -parameters




### -param hThread [in]

A handle to the thread that is to be suspended. 




The handle must have the THREAD_SUSPEND_RESUME access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is the thread's previous suspend count; otherwise, it is (DWORD) -1. To get extended error information, use the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



If the function succeeds, execution of the specified thread is suspended and the thread's suspend count is incremented. Suspending a thread causes the thread to stop executing user-mode (application) code.

This function is primarily designed for use by debuggers. It is not intended to be used for thread synchronization. Calling 
<b>Wow64SuspendThread</b> on a thread that owns a synchronization object, such as a mutex or critical section, can lead to a deadlock if the calling thread tries to obtain a synchronization object owned by a suspended thread. To avoid this situation, a thread within an application that is not a debugger should signal the other thread to suspend itself. The target thread must be designed to watch for this signal and respond appropriately.

Each thread has a suspend count (with a maximum value of MAXIMUM_SUSPEND_COUNT). If the suspend count is greater than zero, the thread is suspended; otherwise, the thread is not suspended and is eligible for execution. Calling 
<b>Wow64SuspendThread</b> causes the target thread's suspend count to be incremented. Attempting to increment past the maximum suspend count causes an error without incrementing the count.

The 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a> function decrements the suspend count of a suspended thread.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and set the last error code to ERROR_INVALID_FUNCTION. A 32-bit application can call this function on a WOW64 thread; the result is the same as calling the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread">SuspendThread</a> function.




## -see-also




<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a>



<a href="/windows/desktop/ProcThread/suspending-thread-execution">Suspending Thread Execution</a>
 

 