---
UID: NF:threadpoolapiset.SetThreadpoolThreadMinimum
title: SetThreadpoolThreadMinimum function (threadpoolapiset.h)
description: Sets the minimum number of threads that the specified thread pool must make available to process callbacks.
helpviewer_keywords: ["SetThreadpoolThreadMinimum","SetThreadpoolThreadMinimum function","base.setthreadpoolthreadminimum","threadpoolapiset/SetThreadpoolThreadMinimum","winbase/SetThreadpoolThreadMinimum"]
old-location: base\setthreadpoolthreadminimum.htm
tech.root: backup
ms.assetid: 39ab262d-50ff-4aaa-93a8-ded2b0f72615
ms.date: 12/05/2018
ms.keywords: SetThreadpoolThreadMinimum, SetThreadpoolThreadMinimum function, base.setthreadpoolthreadminimum, threadpoolapiset/SetThreadpoolThreadMinimum, winbase/SetThreadpoolThreadMinimum
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
 - SetThreadpoolThreadMinimum
 - threadpoolapiset/SetThreadpoolThreadMinimum
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
 - SetThreadpoolThreadMinimum
---

# SetThreadpoolThreadMinimum function


## -description

Sets the minimum number of threads that the specified thread pool must make available to process callbacks.

## -parameters

### -param ptpp [in, out]

A pointer to a <b>TP_POOL</b> structure that defines the thread pool. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this pointer.

### -param cthrdMic [in]

The minimum number of threads.

## -returns

If the function succeeds, it returns TRUE.

If the function fails, it returns FALSE. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To specify the maximum number of threads that  the pool may allocate, call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool">CloseThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>