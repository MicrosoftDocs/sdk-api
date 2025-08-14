---
UID: NF:processthreadsapi.SetThreadPriorityBoost
title: SetThreadPriorityBoost function (processthreadsapi.h)
description: Disables or enables the ability of the system to temporarily boost the priority of a thread.
helpviewer_keywords: ["SetThreadPriorityBoost","SetThreadPriorityBoost function","_win32_setthreadpriorityboost","base.setthreadpriorityboost","processthreadsapi/SetThreadPriorityBoost","winbase/SetThreadPriorityBoost"]
old-location: base\setthreadpriorityboost.htm
tech.root: processthreadsapi
ms.assetid: 5cc16bfe-6792-40e8-91ef-6f54a38e6e33
ms.date: 12/05/2018
ms.keywords: SetThreadPriorityBoost, SetThreadPriorityBoost function, _win32_setthreadpriorityboost, base.setthreadpriorityboost, processthreadsapi/SetThreadPriorityBoost, winbase/SetThreadPriorityBoost
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
 - SetThreadPriorityBoost
 - processthreadsapi/SetThreadPriorityBoost
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
 - SetThreadPriorityBoost
---

# SetThreadPriorityBoost function


## -description

Disables or enables the ability of the system to temporarily boost the priority of a thread.

## -parameters

### -param hThread [in]

A handle to the thread whose priority is to be boosted. The handle must have the <b>THREAD_SET_INFORMATION</b> or <b>THREAD_SET_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_SET_INFORMATION</b> access right.

### -param bDisablePriorityBoost [in]

If this parameter is <b>TRUE</b>, dynamic boosting is disabled. If the parameter is <b>FALSE</b>, dynamic boosting is enabled.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When a thread is running in one of the dynamic priority classes, the system temporarily boosts the thread's priority when it is taken out of a wait state. If 
<b>SetThreadPriorityBoost</b> is called with the <i>DisablePriorityBoost</i> parameter set to <b>TRUE</b>, the thread's priority is not boosted. To restore normal behavior, call 
<b>SetThreadPriorityBoost</b> with <i>DisablePriorityBoost</i> set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost">GetThreadPriorityBoost</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/priority-boosts">Priority Boosts</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>