---
UID: NF:threadpoolapiset.CloseThreadpoolWait
title: CloseThreadpoolWait function (threadpoolapiset.h)
description: Releases the specified wait object.
helpviewer_keywords: ["CloseThreadpoolWait","CloseThreadpoolWait function","base.closethreadpoolwait","threadpoolapiset/CloseThreadpoolWait","winbase/CloseThreadpoolWait"]
old-location: base\closethreadpoolwait.htm
tech.root: backup
ms.assetid: f8323ad2-c0b6-4e5c-b6eb-7195673f8992
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolWait, CloseThreadpoolWait function, base.closethreadpoolwait, threadpoolapiset/CloseThreadpoolWait, winbase/CloseThreadpoolWait
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
 - CloseThreadpoolWait
 - threadpoolapiset/CloseThreadpoolWait
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
 - CloseThreadpoolWait
---

# CloseThreadpoolWait function


## -description

Releases the specified wait object.

## -parameters

### -param pwa [in, out]

A pointer to a <b>TP_WAIT</b> structure that defines the wait object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this pointer.

## -remarks

The wait object is freed immediately if there are no outstanding callbacks; otherwise, the timer object is freed asynchronously after the outstanding callbacks complete.

In some cases, callback functions might run after <b>CloseThreadpoolWait</b> has been called. To prevent this behavior: 

* Call the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a> function
or <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex">SetThreadpoolWaitEx</a> function
with the <i>h</i> parameter set to NULL.
* Call the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a> function with the <i>fCancelPendingCallbacks</i> parameter set to TRUE.
* Call <b>CloseThreadpoolWait</b>.

If there is a cleanup group associated with the wait object, it is not necessary to call this function; calling the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex">SetThreadpoolWaitEx</a>

<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>