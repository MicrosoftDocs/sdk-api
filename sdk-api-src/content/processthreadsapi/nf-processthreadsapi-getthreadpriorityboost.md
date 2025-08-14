---
UID: NF:processthreadsapi.GetThreadPriorityBoost
title: GetThreadPriorityBoost function (processthreadsapi.h)
description: Retrieves the priority boost control state of the specified thread.
helpviewer_keywords: ["GetThreadPriorityBoost","GetThreadPriorityBoost function","_win32_getthreadpriorityboost","base.getthreadpriorityboost","processthreadsapi/GetThreadPriorityBoost","winbase/GetThreadPriorityBoost"]
old-location: base\getthreadpriorityboost.htm
tech.root: processthreadsapi
ms.assetid: 44edf5e3-7543-482f-89ff-ae9daf495ff3
ms.date: 12/05/2018
ms.keywords: GetThreadPriorityBoost, GetThreadPriorityBoost function, _win32_getthreadpriorityboost, base.getthreadpriorityboost, processthreadsapi/GetThreadPriorityBoost, winbase/GetThreadPriorityBoost
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - GetThreadPriorityBoost
 - processthreadsapi/GetThreadPriorityBoost
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadPriorityBoost
---

# GetThreadPriorityBoost function


## -description

Retrieves the priority boost control state of the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread. The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.

### -param pDisablePriorityBoost [out]

A pointer to a variable that receives the priority boost control state. A value of TRUE indicates that dynamic boosting is disabled. A value of FALSE indicates normal behavior.

## -returns

If the function succeeds, the return value is nonzero. In that case, the variable pointed to by the <i>pDisablePriorityBoost</i> parameter receives the priority boost control state.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/priority-boosts">Priority Boosts</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost">SetThreadPriorityBoost</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>