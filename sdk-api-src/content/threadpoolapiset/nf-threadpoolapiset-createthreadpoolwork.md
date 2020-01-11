---
UID: NF:threadpoolapiset.CreateThreadpoolWork
title: CreateThreadpoolWork function (threadpoolapiset.h)
description: Creates a new work object.
old-location: base\createthreadpoolwork.htm
tech.root: ProcThread
ms.assetid: 50647d87-1768-4918-8376-a6a04daca621
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolWork, CreateThreadpoolWork function, base.createthreadpoolwork, threadpoolapiset/CreateThreadpoolWork
f1_keywords:
- threadpoolapiset/CreateThreadpoolWork
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateThreadpoolWork function


## -description


Creates a new work object.


## -parameters




### -param pfnwk [in]

The callback function. A worker thread calls this callback each time you call <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a> to post the work object. For details, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms687396(v=vs.85)">WorkCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the  environment in which to execute the callback. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_WORK</b> structure that defines the work object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork">SubmitThreadpoolWork</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks">WaitForThreadpoolWorkCallbacks</a>
 

 

