---
UID: NF:realtimeapiset.QueryProcessCycleTime
title: QueryProcessCycleTime function (realtimeapiset.h)
description: Retrieves the sum of the cycle time of all threads of the specified process.
helpviewer_keywords: ["QueryProcessCycleTime","QueryProcessCycleTime function","base.queryprocesscycletime","realtimeapiset/QueryProcessCycleTime","winbase/QueryProcessCycleTime"]
old-location: base\queryprocesscycletime.htm
tech.root: backup
ms.assetid: 1859bc0f-8065-4104-b421-1b4c020ad5ea
ms.date: 09/26/2024
ms.keywords: QueryProcessCycleTime, QueryProcessCycleTime function, base.queryprocesscycletime, realtimeapiset/QueryProcessCycleTime, winbase/QueryProcessCycleTime
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
 - QueryProcessCycleTime
 - realtimeapiset/QueryProcessCycleTime
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
 - QueryProcessCycleTime
---

# QueryProcessCycleTime function


## -description

Retrieves the sum of the cycle time of all threads of the specified process.

## -parameters

### -param ProcessHandle [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param CycleTime [out]

The number of CPU clock cycles used by the threads of the process. This value includes cycles spent in both user mode and kernel mode.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To enumerate the processes in the system, use the 
<a href="/windows/desktop/api/psapi/nf-psapi-enumprocesses">EnumProcesses</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.

## -see-also

<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime">QueryIdleProcessorCycleTime</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime">QueryThreadCycleTime</a>