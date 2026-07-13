---
UID: NF:threadpoolapiset.SubmitThreadpoolWork
title: SubmitThreadpoolWork function (threadpoolapiset.h)
description: Posts a work object to the thread pool. A worker thread calls the work object's callback function.
helpviewer_keywords: ["SubmitThreadpoolWork","SubmitThreadpoolWork function","base.submitthreadpoolwork","threadpoolapiset/SubmitThreadpoolWork","winbase/SubmitThreadpoolWork"]
old-location: base\submitthreadpoolwork.htm
tech.root: backup
ms.assetid: 28df173d-b78c-4158-97d5-63117a2d3967
ms.date: 12/05/2018
ms.keywords: SubmitThreadpoolWork, SubmitThreadpoolWork function, base.submitthreadpoolwork, threadpoolapiset/SubmitThreadpoolWork, winbase/SubmitThreadpoolWork
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
 - SubmitThreadpoolWork
 - threadpoolapiset/SubmitThreadpoolWork
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
 - SubmitThreadpoolWork
---

# SubmitThreadpoolWork function


## -description

Posts a work object to the thread pool. A worker thread calls the work object's callback function.

## -parameters

### -param pwk [in, out]

A pointer to a <b>TP_WORK</b> structure that defines the work object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a> function returns this pointer.

## -remarks

You can post a work object one or more times (up to MAXULONG) without waiting for prior callbacks to complete.  The callbacks will execute in parallel. To improve efficiency, the thread pool may throttle the threads.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork">CreateThreadpoolWork</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks">WaitForThreadpoolWorkCallbacks</a>