---
UID: NF:threadpoolapiset.CallbackMayRunLong
title: CallbackMayRunLong function
author: windows-sdk-content
description: Indicates that the callback may not return quickly.
old-location: base\callbackmayrunlong.htm
tech.root: procthread
ms.assetid: 59364b91-d78b-46e2-b298-42f77e712577
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CallbackMayRunLong, CallbackMayRunLong function, base.callbackmayrunlong, threadpoolapiset/CallbackMayRunLong, winbase/CallbackMayRunLong
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - CallbackMayRunLong
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CallbackMayRunLong function


## -description


Indicates that the callback may not return quickly.


## -parameters




### -param pci [in, out]

A <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The structure is passed to the callback function.


## -returns



The function returns TRUE if another thread in the thread pool is available for processing callbacks or the thread pool was able to spin up a new thread.  In this case, the current callback function may use the current thread indefinitely.

The function returns FALSE if another thread in the thread pool is not available to process callbacks and the thread pool was not able to spin up a new thread.  The thread pool will attempt to spin up a new thread after a delay, but if the current callback function runs long, the thread pool may lose efficiency.




## -remarks



The thread pool may use this information to better determine when a new thread should be created.

The <b>CallbackMayRunLong</b> function should be called only by the thread that is processing the callback. Calling this function from another thread may cause a race condition.

The <b>CallbackMayRunLong</b> function always marks the callback as long-running, whether or not a thread is available for processing callbacks or the threadpool is able to allocate a new thread. Therefore, this function should be called only once, even if it returns FALSE. 

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/f25f936c-2570-4e8c-807b-42000cd878bb">DisassociateCurrentThreadFromCallback</a>



<a href="https://msdn.microsoft.com/a29ba988-5d66-4914-9e37-a229bce75af2">FreeLibraryWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/43ce27ee-207c-4317-9771-d82f1f4edda2">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/0e82c041-8191-477d-8a2e-819b8920bbc8">ReleaseMutexWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/d5c8d6a0-6bb1-4ecb-aaba-665d81cb3d14">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/50e127bc-d518-4f84-88ea-b262572d5248">SetEventWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/689d197e-195f-419c-9317-b30c614038c4">TrySubmitThreadpoolCallback</a>
 

 

