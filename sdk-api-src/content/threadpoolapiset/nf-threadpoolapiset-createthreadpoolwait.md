---
UID: NF:threadpoolapiset.CreateThreadpoolWait
title: CreateThreadpoolWait function (threadpoolapiset.h)
description: Creates a new wait object.
helpviewer_keywords: ["CreateThreadpoolWait","CreateThreadpoolWait function","base.createthreadpoolwait","threadpoolapiset/CreateThreadpoolWait","winbase/CreateThreadpoolWait"]
old-location: base\createthreadpoolwait.htm
tech.root: backup
ms.assetid: ba19f5f9-d4b0-4865-9609-95e7697d61c0
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolWait, CreateThreadpoolWait function, base.createthreadpoolwait, threadpoolapiset/CreateThreadpoolWait, winbase/CreateThreadpoolWait
f1_keywords:
- threadpoolapiset/CreateThreadpoolWait
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
- CreateThreadpoolWait
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateThreadpoolWait function


## -description


Creates a new wait object.


## -parameters




### -param pfnwa [in]

The callback function to call when the wait completes or times out. For details, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms687017(v=vs.85)">WaitCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_WAIT</b> structure that defines the wait object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To set the wait object, call the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a> function.

The work item and all functions it calls must be thread-pool safe. Therefore, you cannot call an asynchronous call that requires a persistent thread, such as the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regnotifychangekeyvalue">RegNotifyChangeKeyValue</a> function, from the default callback environment. Instead, set the thread pool maximum equal to the thread pool minimum using the <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum">SetThreadpoolThreadMaximum</a> and <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum">SetThreadpoolThreadMinimum</a> functions, or create your own thread using the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a> function.

<b>Windows 8:  </b><a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regnotifychangekeyvalue">RegNotifyChangeKeyValue</a> can be called from a work item by setting the REG_NOTIFY_THREAD_AGNOSTIC flag.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>
 

 

