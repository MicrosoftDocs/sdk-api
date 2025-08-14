---
UID: NF:realtimeapiset.QueryThreadCycleTime
title: QueryThreadCycleTime function (realtimeapiset.h)
description: Retrieves the cycle time for the specified thread.
helpviewer_keywords: ["QueryThreadCycleTime","QueryThreadCycleTime function","base.querythreadcycletime","realtimeapiset/QueryThreadCycleTime","winbase/QueryThreadCycleTime"]
old-location: base\querythreadcycletime.htm
tech.root: backup
ms.assetid: 5828b073-48af-4118-9206-096b87c978e7
ms.date: 09/26/2024
ms.keywords: QueryThreadCycleTime, QueryThreadCycleTime function, base.querythreadcycletime, realtimeapiset/QueryThreadCycleTime, winbase/QueryThreadCycleTime
req.header: realtimeapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryThreadCycleTime
 - realtimeapiset/QueryThreadCycleTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-realtime-l1-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-realtime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-RealTime-l1-1-1.dll
api_name:
 - QueryThreadCycleTime
---

# QueryThreadCycleTime function


## -description

Retrieves the cycle time for the specified thread.

## -parameters

### -param ThreadHandle [in]

A handle to the thread. The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/win32/procthread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param CycleTime [out]

The number of CPU clock cycles used by the thread. This value includes cycles spent in both user mode and kernel mode.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To enumerate the threads of the process, use the <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a> and <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32next">Thread32Next</a> functions. To get the thread handle for a thread identifier, use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function.

Do not attempt to convert the CPU clock cycles returned by <b>QueryThreadCycleTime</b> to elapsed time. This function uses timer services provided by the CPU, which can vary in implementation. For example, some CPUs will vary the frequency of the timer when changing the frequency at which the CPU runs and others will leave it at a fixed rate. The behavior of each CPU is described in the documentation provided by the CPU vendor.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.

## -see-also

<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime">QueryIdleProcessorCycleTime</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime">QueryProcessCycleTime</a>
