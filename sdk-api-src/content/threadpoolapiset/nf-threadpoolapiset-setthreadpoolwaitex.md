---
UID: NF:threadpoolapiset.SetThreadpoolWaitEx
title: SetThreadpoolWaitEx function (threadpoolapiset.h)
description: Sets the wait object replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the handle becomes signaled or after the specified timeout expires. (SetThreadpoolWaitEx)
helpviewer_keywords: ["SetThreadpoolWaitEx","SetThreadpoolWaitEx function","base.setthreadpoolwaitex","threadpoolapiset/SetThreadpoolWaitEx"]
old-location: base\setthreadpoolwaitex.htm
tech.root: backup
ms.assetid: 0653D169-CE6B-4D8F-A640-F49B2BCBBF61
ms.date: 12/05/2018
ms.keywords: SetThreadpoolWaitEx, SetThreadpoolWaitEx function, base.setthreadpoolwaitex, threadpoolapiset/SetThreadpoolWaitEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadpoolWaitEx
 - threadpoolapiset/SetThreadpoolWaitEx
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
 - SetThreadpoolWaitEx
---

# SetThreadpoolWaitEx function


## -description

Sets the wait object, replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the handle becomes signaled or after the specified timeout expires.

## -parameters

### -param pwa [in, out]

A pointer to a <b>TP_WAIT</b> structure that defines the wait object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this pointer.

### -param h [in, optional]

A handle.

If this parameter is NULL, the wait object will cease to queue new callbacks (but callbacks already queued will still occur).

If this parameter is not NULL, it must refer to a valid waitable object.

If this handle is closed while the wait is still pending, the function's behavior is undefined. If the wait is still pending and the handle must be closed, use <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a> to cancel the wait and then close the handle.

The wait is considered set if this parameter is non-NULL.

### -param pftTimeout [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the absolute or relative time at which the wait operation should time out.  If this parameter points to a positive value, it indicates the absolute time since January 1, 1601 (UTC), in 100-nanosecond intervals. If this parameter points to a negative value, it indicates the amount of time to wait relative to the current time. If this parameter points to zero, then the wait times out immediately. For more information about time values, see <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

If this parameter is NULL, then the wait does not time out.

### -param Reserved

Reserved.
Must be NULL.

## -returns

Returns TRUE if the wait was previously set and was canceled.
Otherwise returns FALSE.

If the wait's previous state was "set", and the function returns FALSE, then a callback is in progress or about to commence.
See the remarks for further discussion.

## -remarks

A wait object can wait for only one handle. Setting the handle for a wait object replaces the previous wait handle, if any.

In some cases, callback functions might run after an application closes the threadpool timer. To prevent this behavior, an application should follow the steps described in <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>.

If the timeout specified by <i>pftTimeout</i> is relative, the time that the system spends in sleep or hibernation does not count toward the expiration of the wait. The wait is signaled when the cumulative amount of elapsed time the system spends in the waking state equals the wait's relative timeout. If the timeout specified by <i>pftTimeout</i> is absolute, the time that the system spends in sleep or hibernation does count toward the expiration of the wait. If the wait expires while the system is sleeping, the wait is signaled immediately when the system wakes.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>
