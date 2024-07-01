---
UID: NF:threadpoolapiset.SetThreadpoolWait
title: SetThreadpoolWait function (threadpoolapiset.h)
description: Sets the wait object�replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the handle becomes signaled or after the specified timeout expires. (SetThreadpoolWait)
helpviewer_keywords: ["SetThreadpoolWait","SetThreadpoolWait function","base.setthreadpoolwait","threadpoolapiset/SetThreadpoolWait","winbase/SetThreadpoolWait"]
old-location: base\setthreadpoolwait.htm
tech.root: backup
ms.assetid: ebd0ecad-a864-43cf-a1cb-e4c2d595ef81
ms.date: 12/05/2018
ms.keywords: SetThreadpoolWait, SetThreadpoolWait function, base.setthreadpoolwait, threadpoolapiset/SetThreadpoolWait, winbase/SetThreadpoolWait
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
 - SetThreadpoolWait
 - threadpoolapiset/SetThreadpoolWait
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
 - SetThreadpoolWait
---

# SetThreadpoolWait function


## -description

Sets the wait object, replacing the previous wait object, if any. A worker thread calls the wait object's callback function after the  handle becomes signaled or after the specified timeout expires.

## -parameters

### -param pwa [in, out]

A pointer to a <b>TP_WAIT</b> structure that defines the wait object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this pointer.

### -param h [in, optional]

A handle.

If this parameter is NULL, the wait object will cease to queue new callbacks (but callbacks already queued will still occur).

If this parameter is not NULL, it must refer to a valid waitable object. 

Mutex is not supported. If a handle to a mutex is passed in, the thread pool raises a STATUS_THREADPOOL_HANDLE_EXCEPTION exception and ExceptionRecord.ExceptionInformation[0] will be equal to STATUS_INVALID_PARAMETER_3.

If this handle is closed while the wait is still pending, the function's behavior is undefined. If the wait is still pending and the handle must be closed, use <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a> to cancel the wait and then close the handle.

The wait is considered set if this parameter is non-NULL.

### -param pftTimeout [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the absolute or relative time at which the wait operation should time out.  If this parameter points to a positive value, it indicates the absolute time since January 1, 1601 (UTC), in 100-nanosecond intervals. If this parameter points to a negative value, it indicates the amount of time to wait relative to the current time. For more information about time values, see <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

If this parameter points to 0, the wait times out immediately. If this parameter is NULL, the wait will not time out.

## -remarks

A wait object can wait for only one handle. Setting the handle for a wait object replaces the previous handle, if any.

You must re-register the event with the wait object  before signaling it each time to trigger the wait callback.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex">SetThreadpoolWaitEx</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>
