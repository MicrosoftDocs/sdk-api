---
UID: NF:threadpoolapiset.ReleaseMutexWhenCallbackReturns
title: ReleaseMutexWhenCallbackReturns function (threadpoolapiset.h)
description: Specifies the mutex that the thread pool will release when the current callback completes.
old-location: base\releasemutexwhencallbackreturns.htm
tech.root: ProcThread
ms.assetid: 0e82c041-8191-477d-8a2e-819b8920bbc8
ms.date: 12/05/2018
ms.keywords: ReleaseMutexWhenCallbackReturns, ReleaseMutexWhenCallbackReturns function, base.releasemutexwhencallbackreturns, threadpoolapiset/ReleaseMutexWhenCallbackReturns, winbase/ReleaseMutexWhenCallbackReturns
f1_keywords:
- threadpoolapiset/ReleaseMutexWhenCallbackReturns
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
- ReleaseMutexWhenCallbackReturns
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReleaseMutexWhenCallbackReturns function


## -description


Specifies the mutex that the thread pool will release when the current callback completes.


## -parameters




### -param pci [in, out]

A <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The structure is passed to the callback function.


### -param mut [in]

A handle to the mutex.


## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong">CallbackMayRunLong</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback">DisassociateCurrentThreadFromCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns">SetEventWhenCallbackReturns</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback">TrySubmitThreadpoolCallback</a>
 

 

