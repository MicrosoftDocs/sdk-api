---
UID: NF:threadpoolapiset.CloseThreadpoolWait
title: CloseThreadpoolWait function (threadpoolapiset.h)
description: Releases the specified wait object.
old-location: base\closethreadpoolwait.htm
tech.root: ProcThread
ms.assetid: f8323ad2-c0b6-4e5c-b6eb-7195673f8992
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolWait, CloseThreadpoolWait function, base.closethreadpoolwait, threadpoolapiset/CloseThreadpoolWait, winbase/CloseThreadpoolWait
f1_keywords:
- threadpoolapiset/CloseThreadpoolWait
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
- CloseThreadpoolWait
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseThreadpoolWait function


## -description


Releases the specified wait object.


## -parameters




### -param pwa [in, out]

A <b>TP_WAIT</b> structure that defines the wait object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this structure.


## -remarks



The wait object is freed immediately if there are no outstanding callbacks; otherwise, the timer object is freed asynchronously after the outstanding callbacks complete.

If there is a cleanup group associated with the wait object, it is not necessary to call this function; calling the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers">CloseThreadpoolCleanupGroupMembers</a> function releases the  work, wait, and timer objects associated with the cleanup group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>
 

 

