---
UID: NF:threadpoolapiset.CloseThreadpool
title: CloseThreadpool function (threadpoolapiset.h)
description: Closes the specified thread pool.
helpviewer_keywords: ["CloseThreadpool","CloseThreadpool function","base.closethreadpool","threadpoolapiset/CloseThreadpool","winbase/CloseThreadpool"]
old-location: base\closethreadpool.htm
tech.root: backup
ms.assetid: 84f673b5-d9b1-4f3d-9ae6-b1ad173268cd
ms.date: 12/05/2018
ms.keywords: CloseThreadpool, CloseThreadpool function, base.closethreadpool, threadpoolapiset/CloseThreadpool, winbase/CloseThreadpool
req.header: threadpoolapiset.h
req.include-header: Windows.h
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
 - CloseThreadpool
 - threadpoolapiset/CloseThreadpool
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
 - CloseThreadpool
---

# CloseThreadpool function


## -description

Closes the specified thread pool.

## -parameters

### -param ptpp [in, out]

A pointer to a <b>TP_POOL</b> structure that defines the thread pool. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this pointer.

## -remarks

The thread pool is closed immediately if there are no outstanding <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">work</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">I/O</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">timer</a>, or <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">wait</a> objects that are bound to the pool; otherwise, the thread pool is released asynchronously after the outstanding objects are freed.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>