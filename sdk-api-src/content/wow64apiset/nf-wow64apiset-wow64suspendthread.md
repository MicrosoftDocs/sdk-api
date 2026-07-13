---
UID: NF:wow64apiset.Wow64SuspendThread
title: Wow64SuspendThread
ms.date: 08/19/2020
targetos: Windows
description: Suspends the specified WOW64 thread.
tech.root: fs
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: wow64apiset.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - Kernel32.dll
api_name:
 - Wow64SuspendThread
f1_keywords:
 - Wow64SuspendThread
 - wow64apiset/Wow64SuspendThread
helpviewer_keywords:
 - Wow64SuspendThread
dev_langs:
 - c++
---

# Wow64SuspendThread function

## -description

Suspends the specified WOW64 thread.

## -parameters

### -param hThread

A handle to the thread that is to be suspended. The handle must have the THREAD_SUSPEND_RESUME access right. For more information, see [Thread Security and Access Rights](/windows/win32/procthread/thread-security-and-access-rights).

## -returns

If the function succeeds, the return value is the thread's previous suspend count; otherwise, it is (DWORD) -1. To get extended error information, use the [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) function.

## -remarks

If the function succeeds, execution of the specified thread is suspended and the thread's suspend count is incremented. Suspending a thread causes the thread to stop executing user-mode (application) code.

This function is primarily designed for use by debuggers. It is not intended to be used for thread synchronization. Calling **Wow64SuspendThread** on a thread that owns a synchronization object, such as a mutex or critical section, can lead to a deadlock if the calling thread tries to obtain a synchronization object owned by a suspended thread. To avoid this situation, a thread within an application that is not a debugger should signal the other thread to suspend itself. The target thread must be designed to watch for this signal and respond appropriately.

Each thread has a suspend count (with a maximum value of MAXIMUM_SUSPEND_COUNT). If the suspend count is greater than zero, the thread is suspended; otherwise, the thread is not suspended and is eligible for execution. Calling 
**Wow64SuspendThread** causes the target thread's suspend count to be incremented. Attempting to increment past the maximum suspend count causes an error without incrementing the count.

The [ResumeThread](../processthreadsapi/nf-processthreadsapi-resumethread.md) function decrements the suspend count of a suspended thread.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and set the last error code to ERROR_INVALID_FUNCTION. A 32-bit application can call this function on a WOW64 thread; the result is the same as calling the [SuspendThread](../processthreadsapi/nf-processthreadsapi-suspendthread.md) function.

## -see-also

[ResumeThread](../processthreadsapi/nf-processthreadsapi-resumethread.md)