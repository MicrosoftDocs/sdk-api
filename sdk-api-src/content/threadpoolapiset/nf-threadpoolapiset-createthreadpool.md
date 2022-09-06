---
UID: NF:threadpoolapiset.CreateThreadpool
title: CreateThreadpool function (threadpoolapiset.h)
description: Allocates a new pool of threads to execute callbacks.
helpviewer_keywords: ["CreateThreadpool","CreateThreadpool function","base.createthreadpool","threadpoolapiset/CreateThreadpool","winbase/CreateThreadpool"]
old-location: base\createthreadpool.htm
tech.root: backup
ms.assetid: cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6
ms.date: 12/05/2018
ms.keywords: CreateThreadpool, CreateThreadpool function, base.createthreadpool, threadpoolapiset/CreateThreadpool, winbase/CreateThreadpool
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
 - CreateThreadpool
 - threadpoolapiset/CreateThreadpool
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
 - CreateThreadpool
---

# CreateThreadpool function


## -description

Allocates a new pool of threads to execute callbacks.

## -parameters

### -param reserved

This parameter is reserved and must be NULL.

## -returns

If the function succeeds, it returns a pointer to a <b>TP_POOL</b> structure representing the newly allocated thread pool. Applications do not modify the members of this structure.

If function fails, it returns NULL. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After creating the new thread pool, you should call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a> to specify the maximum number of threads that the pool can allocate and <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a> to specify the minimum number of threads available in the pool.

To use the pool, you must associate the pool with a callback environment. To create the callback environment, call <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>. Then, call <a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpool">SetThreadpoolCallbackPool</a> to associate the pool with the callback environment.

To release the thread pool, call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool">CloseThreadpool</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool">CloseThreadpool</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>