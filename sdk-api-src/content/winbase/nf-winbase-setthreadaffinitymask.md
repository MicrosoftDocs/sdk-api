---
UID: NF:winbase.SetThreadAffinityMask
title: SetThreadAffinityMask function (winbase.h)
description: Sets a processor affinity mask for the specified thread.
helpviewer_keywords: ["SetThreadAffinityMask","SetThreadAffinityMask function","_win32_setthreadaffinitymask","base.setthreadaffinitymask","winbase/SetThreadAffinityMask"]
old-location: base\setthreadaffinitymask.htm
tech.root: backup
ms.assetid: 3390930d-026f-4f86-97bc-1da34bb384ba
ms.date: 12/05/2018
ms.keywords: SetThreadAffinityMask, SetThreadAffinityMask function, _win32_setthreadaffinitymask, base.setthreadaffinitymask, winbase/SetThreadAffinityMask
req.header: winbase.h
req.include-header: Windows.h
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
 - SetThreadAffinityMask
 - winbase/SetThreadAffinityMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-l1-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetThreadAffinityMask
---

# SetThreadAffinityMask function


## -description

Sets a processor affinity mask for the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread whose affinity mask is to be set.

This handle must have the <b>THREAD_SET_INFORMATION</b> or <b>THREAD_SET_LIMITED_INFORMATION</b> access right and the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_SET_INFORMATION</b> and <b>THREAD_QUERY_INFORMATION</b> access rights.

### -param dwThreadAffinityMask [in]

The affinity mask for the thread.

On a system with more than 64 processors, the affinity mask must specify processors in the thread's current <a href="/windows/desktop/ProcThread/processor-groups">processor group</a>.

## -returns

If the function succeeds, the return value is the thread's previous affinity mask.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the thread affinity mask requests a processor that is not selected for the process affinity mask, the last error code is <b>ERROR_INVALID_PARAMETER</b>.

## -remarks

A thread affinity mask is a bit vector in which each bit represents a logical processor that a thread is allowed to run on. A thread affinity mask must be a subset of the process affinity mask for the containing process of a thread. A thread can only run on the processors its process can run on. Therefore, the thread affinity mask cannot specify a 1 bit for a processor when the process affinity mask specifies a 0 bit for that processor.

Setting an affinity mask for a process or thread can result in threads receiving less processor time, as the system is restricted from running the threads on certain processors. In most cases, it is better to let the system select an available processor.

If the new thread affinity mask does not specify the processor that is currently running the thread, the thread is rescheduled on one of the allowable processors.

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default. The <i>dwThreadAffinityMask</i> must specify processors in the thread's current primary group.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/processor-groups">Processor Groups</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setprocessaffinitymask">SetProcessAffinityMask</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor">SetThreadIdealProcessor</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>
