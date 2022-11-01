---
UID: NF:processthreadsapi.GetCurrentThreadId
title: GetCurrentThreadId function (processthreadsapi.h)
description: Retrieves the thread identifier of the calling thread.
helpviewer_keywords: ["GetCurrentThreadId","GetCurrentThreadId function","_win32_getcurrentthreadid","base.getcurrentthreadid","processthreadsapi/GetCurrentThreadId","winbase/GetCurrentThreadId"]
old-location: base\getcurrentthreadid.htm
tech.root: processthreadsapi
ms.assetid: a496f61a-e027-44e7-8b22-4f6651d7afb2
ms.date: 12/05/2018
ms.keywords: GetCurrentThreadId, GetCurrentThreadId function, _win32_getcurrentthreadid, base.getcurrentthreadid, processthreadsapi/GetCurrentThreadId, winbase/GetCurrentThreadId
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetCurrentThreadId
 - processthreadsapi/GetCurrentThreadId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - vertdll.dll
api_name:
 - GetCurrentThreadId
---

# GetCurrentThreadId function


## -description

Retrieves the thread identifier of the calling thread.



## -returns

The return value is the thread identifier of the calling thread.

## -remarks

Until the thread terminates, the thread identifier uniquely identifies the thread throughout the system.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/using-thread-local-storage">Using Thread Local Storage</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>
