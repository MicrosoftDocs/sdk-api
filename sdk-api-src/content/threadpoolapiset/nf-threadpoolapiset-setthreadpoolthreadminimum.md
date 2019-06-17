---
UID: NF:threadpoolapiset.SetThreadpoolThreadMinimum
title: SetThreadpoolThreadMinimum function (threadpoolapiset.h)
author: windows-sdk-content
description: Sets the minimum number of threads that the specified thread pool must make available to process callbacks.
old-location: base\setthreadpoolthreadminimum.htm
tech.root: ProcThread
ms.assetid: 39ab262d-50ff-4aaa-93a8-ded2b0f72615
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetThreadpoolThreadMinimum, SetThreadpoolThreadMinimum function, base.setthreadpoolthreadminimum, threadpoolapiset/SetThreadpoolThreadMinimum, winbase/SetThreadpoolThreadMinimum
ms.topic: function
f1_keywords: ["threadpoolapiset/SetThreadpoolThreadMinimum"]
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
 - SetThreadpoolThreadMinimum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadpoolThreadMinimum function


## -description


Sets the minimum number of threads that the specified thread pool must make available to process callbacks.


## -parameters




### -param ptpp [in, out]

A <b>TP_POOL</b> structure that defines the thread pool. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this structure.


### -param cthrdMic [in]

The minimum number of threads.


## -returns



If the function succeeds, it returns TRUE.

If the function fails, it returns FALSE. To retrieve extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To specify the maximum number of threads that  the pool may allocate, call <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool">CloseThreadpool</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

