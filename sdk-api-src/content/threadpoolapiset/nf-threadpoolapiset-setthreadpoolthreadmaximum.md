---
UID: NF:threadpoolapiset.SetThreadpoolThreadMaximum
title: SetThreadpoolThreadMaximum function (threadpoolapiset.h)
description: Sets the maximum number of threads that the specified thread pool can allocate to process callbacks.
helpviewer_keywords: ["SetThreadpoolThreadMaximum","SetThreadpoolThreadMaximum function","base.setthreadpoolthreadmaximum","threadpoolapiset/SetThreadpoolThreadMaximum"]
old-location: base\setthreadpoolthreadmaximum.htm
tech.root: backup
ms.assetid: 381849cf-6835-40f2-be68-0522b16e4822
ms.date: 12/05/2018
ms.keywords: SetThreadpoolThreadMaximum, SetThreadpoolThreadMaximum function, base.setthreadpoolthreadmaximum, threadpoolapiset/SetThreadpoolThreadMaximum
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
 - SetThreadpoolThreadMaximum
 - threadpoolapiset/SetThreadpoolThreadMaximum
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
 - SetThreadpoolThreadMaximum
---

# SetThreadpoolThreadMaximum function


## -description

Sets the maximum number of threads that the specified thread pool can allocate to process callbacks.

## -parameters

### -param ptpp [in, out]

A pointer to a <b>TP_POOL</b> structure that defines the thread pool. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this pointer.

### -param cthrdMost [in]

The maximum number of threads.

## -remarks

To specify the minimum number of threads available in the pool, call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool">CloseThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>