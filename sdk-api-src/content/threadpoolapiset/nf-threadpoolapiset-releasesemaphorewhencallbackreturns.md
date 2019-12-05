---
UID: NF:threadpoolapiset.ReleaseSemaphoreWhenCallbackReturns
title: ReleaseSemaphoreWhenCallbackReturns function (threadpoolapiset.h)
description: Specifies the semaphore that the thread pool will release when the current callback completes.
old-location: base\releasesemaphorewhencallbackreturns.htm
tech.root: ProcThread
ms.assetid: d5c8d6a0-6bb1-4ecb-aaba-665d81cb3d14
ms.date: 12/05/2018
ms.keywords: ReleaseSemaphoreWhenCallbackReturns, ReleaseSemaphoreWhenCallbackReturns function, base.releasesemaphorewhencallbackreturns, threadpoolapiset/ReleaseSemaphoreWhenCallbackReturns, winbase/ReleaseSemaphoreWhenCallbackReturns
ms.topic: function
f1_keywords:
- threadpoolapiset/ReleaseSemaphoreWhenCallbackReturns
dev_langs:
- c++
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
- ReleaseSemaphoreWhenCallbackReturns
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReleaseSemaphoreWhenCallbackReturns function


## -description


Specifies the semaphore that the thread pool will release when the current callback completes.


## -parameters




### -param pci [in, out]

A <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The structure is passed to the callback function.


### -param sem [in]

A handle to the semaphore.


### -param crel [in]

The amount by which to increment the semaphore object's count.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong">CallbackMayRunLong</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback">DisassociateCurrentThreadFromCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns">ReleaseMutexWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns">SetEventWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback">TrySubmitThreadpoolCallback</a>
 

 

