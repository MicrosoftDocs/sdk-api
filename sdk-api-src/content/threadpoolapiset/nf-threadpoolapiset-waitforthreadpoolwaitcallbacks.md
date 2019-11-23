---
UID: NF:threadpoolapiset.WaitForThreadpoolWaitCallbacks
title: WaitForThreadpoolWaitCallbacks function (threadpoolapiset.h)

description: Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
old-location: base\waitforthreadpoolwaitcallbacks.htm
tech.root: ProcThread
ms.assetid: 49c40b35-a0ed-40a1-9c35-5d3985ebd98f

ms.date: 12/05/2018
ms.keywords: WaitForThreadpoolWaitCallbacks, WaitForThreadpoolWaitCallbacks function, base.waitforthreadpoolwaitcallbacks, threadpoolapiset/WaitForThreadpoolWaitCallbacks, winbase/WaitForThreadpoolWaitCallbacks
ms.topic: function
f1_keywords: 
 - "threadpoolapiset/WaitForThreadpoolWaitCallbacks"
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
 - WaitForThreadpoolWaitCallbacks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WaitForThreadpoolWaitCallbacks function


## -description


Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.


## -parameters




### -param pwa [in, out]

A <b>TP_WAIT</b> structure that defines the wait object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns the <b>TP_WAIT</b> structure.


### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.


## -returns



This function does not return a value.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

