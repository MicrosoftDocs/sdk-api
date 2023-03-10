---
UID: NF:winbase.SetThreadpoolCallbackPool
title: SetThreadpoolCallbackPool function (winbase.h)
description: Sets the thread pool to be used when generating callbacks.
helpviewer_keywords: ["SetThreadpoolCallbackPool","SetThreadpoolCallbackPool function","base.setthreadpoolcallbackpool","winbase/SetThreadpoolCallbackPool"]
old-location: base\setthreadpoolcallbackpool.htm
tech.root: backup
ms.assetid: 022d83de-ff6c-4bc8-8213-42f403a323e8
ms.date: 12/05/2018
ms.keywords: SetThreadpoolCallbackPool, SetThreadpoolCallbackPool function, base.setthreadpoolcallbackpool, winbase/SetThreadpoolCallbackPool
req.header: winbase.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadpoolCallbackPool
 - winbase/SetThreadpoolCallbackPool
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackPool
---

# SetThreadpoolCallbackPool function


## -description

Sets the thread pool to be used when generating callbacks.

## -parameters

### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

### -param ptpp [in]

A <b>TP_POOL</b> structure that defines the thread pool. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this structure.

## -remarks

If you do not specify a thread pool, the global thread pool is used.

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbacklibrary">SetThreadpoolCallbackLibrary</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpriority">SetThreadpoolCallbackPriority</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackrunslong">SetThreadpoolCallbackRunsLong</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>