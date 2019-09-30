---
UID: NF:realtimeapiset.QueryIdleProcessorCycleTime
title: QueryIdleProcessorCycleTime function (realtimeapiset.h)
author: windows-sdk-content
description: Retrieves the cycle time for the idle thread of each processor in the system.
old-location: base\queryidleprocessorcycletime.htm
tech.root: ProcThread
ms.assetid: 75a5c4cf-ccc7-47ab-a2a9-88051e0a7d06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryIdleProcessorCycleTime, QueryIdleProcessorCycleTime function, base.queryidleprocessorcycletime, realtimeapiset/QueryIdleProcessorCycleTime, winbase/QueryIdleProcessorCycleTime
ms.topic: function
f1_keywords: 
 - "realtimeapiset/QueryIdleProcessorCycleTime"
req.header: realtimeapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - API-MS-Win-Core-realtime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-RealTime-l1-1-1.dll
api_name:
 - QueryIdleProcessorCycleTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryIdleProcessorCycleTime function


## -description


Retrieves the cycle time for the idle thread of each processor in the system.

On a system with more than 64 processors, this function retrieves the cycle time for the idle thread of each processor in the <a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">processor group</a> to which the calling thread is assigned. Use the <a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex">QueryIdleProcessorCycleTimeEx</a> function to retrieve the cycle time for the idle thread on each logical processor for a specific processor group. 


## -parameters




### -param BufferLength [in, out]

On input, specifies the size of the <i>ProcessorIdleCycleTime</i> buffer, in bytes. This buffer is expected to be 8 times the number of processors in the group.

On output, specifies the number of elements written to the buffer. If the buffer size is not sufficient, the function fails and this parameter receives the required length of the buffer.


### -param ProcessorIdleCycleTime [out]

The number of CPU clock cycles used by each idle thread. This buffer must be 8  times the number of processors in the system in size.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">Processor Groups</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex">QueryIdleProcessorCycleTimeEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime">QueryProcessCycleTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime">QueryThreadCycleTime</a>
 

 

