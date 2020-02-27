---
UID: NF:threadpoolapiset.SetThreadpoolWaitEx
title: SetThreadpoolWaitEx function (threadpoolapiset.h)
description: Sets the wait object&#8212;replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the handle becomes signaled or after the specified timeout expires.
old-location: base\setthreadpoolwaitex.htm
tech.root: ProcThread
ms.assetid: 0653D169-CE6B-4D8F-A640-F49B2BCBBF61
ms.date: 12/05/2018
ms.keywords: SetThreadpoolWaitEx, SetThreadpoolWaitEx function, base.setthreadpoolwaitex, threadpoolapiset/SetThreadpoolWaitEx
f1_keywords:
- threadpoolapiset/SetThreadpoolWaitEx
dev_langs:
- c++
req.header: threadpoolapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- SetThreadpoolWaitEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadpoolWaitEx function


## -description


Sets the wait object—replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the handle becomes signaled or after the specified timeout expires.


## -parameters




### -param pwa [in, out]

A pointer to a <b>TP_WAIT</b> structure that defines the wait object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this structure.


### -param h [in, optional]

A handle.



If this parameter is NULL, the wait object will cease to queue new callbacks (but callbacks already queued will still occur).



If this parameter is not NULL, it must refer to a valid waitable object.

If this handle is closed while the wait is still pending, the function's behavior is undefined. If the wait is still pending and the handle must be closed, use <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a> to cancel the wait and then close the handle.



### -param pftTimeout [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the absolute or relative time at which the wait operation should time out.  If this parameter points to a positive value, it indicates the absolute time since January 1, 1601 (UTC), in 100-nanosecond intervals. If this parameter points to a negative value, it indicates the amount of time to wait relative to the current time. For more information about time values, see <a href="https://docs.microsoft.com/windows/desktop/SysInfo/file-times">File Times</a>.


### -param Reserved

Reserved.


## -returns



TRUE, if the timer was previously active and was canceled; otherwise, FALSE. This return value can be used to maintain reference counts to synchronize between completion and cancellation of a non-periodic timer operation. If FALSE is returned, a callback may be in progress or about to commence. If FALSE is returned, a subsequent <b>WaitForThreadpool</b> or <b>WaitForThreadpoolEx</b> Callback operation will complete after that callback is completed. A subsequent <b>SetThreadpool</b> or <b>SetThreadpoolEx</b> operation that is not later canceled will result in an additional callback.”




## -remarks



A wait object can wait for only one handle. Setting the handle for a wait object replaces the previous wait handle, if any.

In some cases, callback functions might run after an application closes the threadpool timer. To prevent this behavior, an application should call <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer">SetThreadpoolTimer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex">SetThreadpoolTimerEx</a> with the <b>pftDueTime</b> parameter set to NULL and the <b>msPeriod</b> and <b>msWindowLength</b> parameters set to 0. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer">CloseThreadpoolTimer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>
 

 

