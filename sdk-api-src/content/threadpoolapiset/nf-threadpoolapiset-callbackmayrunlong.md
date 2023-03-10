---
UID: NF:threadpoolapiset.CallbackMayRunLong
title: CallbackMayRunLong function (threadpoolapiset.h)
description: Indicates that the callback may not return quickly.
helpviewer_keywords: ["CallbackMayRunLong","CallbackMayRunLong function","base.callbackmayrunlong","threadpoolapiset/CallbackMayRunLong","winbase/CallbackMayRunLong"]
old-location: base\callbackmayrunlong.htm
tech.root: backup
ms.assetid: 59364b91-d78b-46e2-b298-42f77e712577
ms.date: 12/05/2018
ms.keywords: CallbackMayRunLong, CallbackMayRunLong function, base.callbackmayrunlong, threadpoolapiset/CallbackMayRunLong, winbase/CallbackMayRunLong
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - CallbackMayRunLong
 - threadpoolapiset/CallbackMayRunLong
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CallbackMayRunLong
---

# CallbackMayRunLong function


## -description

Indicates that the callback may not return quickly.

## -parameters

### -param pci [in, out]

A pointer to a <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The pointer is passed to the callback function.

## -returns

The function returns TRUE if another thread in the thread pool is available for processing callbacks or the thread pool was able to create a new thread.  In this case, the current callback function may use the current thread indefinitely.

The function returns FALSE if another thread in the thread pool is not available to process callbacks and the thread pool was not able to create a new thread.  The thread pool will attempt to create a new thread after a delay, but if the current callback function runs long, the thread pool may lose efficiency.

## -remarks

The thread pool may use this information to better determine when a new thread should be created.

The <b>CallbackMayRunLong</b> function should be called only by the thread that is processing the callback. Calling this function from another thread may cause a race condition.

The <b>CallbackMayRunLong</b> function always marks the callback as long-running, whether or not a thread is available for processing callbacks or the threadpool is able to allocate a new thread. Therefore, this function should be called only once, even if it returns FALSE. 

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback">DisassociateCurrentThreadFromCallback</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns">ReleaseMutexWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns">SetEventWhenCallbackReturns</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback">TrySubmitThreadpoolCallback</a>