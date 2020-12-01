---
UID: NF:threadpoolapiset.CreateThreadpoolWork
title: CreateThreadpoolWork function (threadpoolapiset.h)
description: Creates a new work object.
helpviewer_keywords: ["CreateThreadpoolWork","CreateThreadpoolWork function","base.createthreadpoolwork","threadpoolapiset/CreateThreadpoolWork"]
old-location: base\createthreadpoolwork.htm
tech.root: backup
ms.assetid: 50647d87-1768-4918-8376-a6a04daca621
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolWork, CreateThreadpoolWork function, base.createthreadpoolwork, threadpoolapiset/CreateThreadpoolWork
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
 - CreateThreadpoolWork
 - threadpoolapiset/CreateThreadpoolWork
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
 - CreateThreadpoolWork
---

# CreateThreadpoolWork function


## -description

Creates a new work object.

## -parameters

### -param pfnwk [in]

The callback function. A worker thread calls this callback each time you call <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a> to post the work object. For details, see <a href="/previous-versions/windows/desktop/legacy/ms687396(v=vs.85)">WorkCallback</a>.

### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.

### -param pcbe [in, optional]

A pointer to a <b>TP_CALLBACK_ENVIRON</b> structure that defines the  environment in which to execute the callback. Use the <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function to initialize the structure before calling this function.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.

## -returns

If the function succeeds, it returns a pointer to a <b>TP_WORK</b> structure that defines the work object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks">WaitForThreadpoolWorkCallbacks</a>