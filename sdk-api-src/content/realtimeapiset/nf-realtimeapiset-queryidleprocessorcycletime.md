---
UID: NF:realtimeapiset.QueryIdleProcessorCycleTime
title: QueryIdleProcessorCycleTime function
author: windows-sdk-content
description: Retrieves the cycle time for the idle thread of each processor in the system.
old-location: base\queryidleprocessorcycletime.htm
tech.root: procthread
ms.assetid: 75a5c4cf-ccc7-47ab-a2a9-88051e0a7d06
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: QueryIdleProcessorCycleTime, QueryIdleProcessorCycleTime function, base.queryidleprocessorcycletime, realtimeapiset/QueryIdleProcessorCycleTime, winbase/QueryIdleProcessorCycleTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryIdleProcessorCycleTime function


## -description


Retrieves the cycle time for the idle thread of each processor in the system.

On a system with more than 64 processors, this function retrieves the cycle time for the idle thread of each processor in the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> to which the calling thread is assigned. Use the <a href="https://msdn.microsoft.com/4bf05e40-96d1-4c01-b3a8-8a45934b38c6">QueryIdleProcessorCycleTimeEx</a> function to retrieve the cycle time for the idle thread on each logical processor for a specific processor group. 


## -parameters




### -param BufferLength [in, out]

On input, specifies the size of the <i>ProcessorIdleCycleTime</i> buffer, in bytes. This buffer is expected to be 8 times the number of processors in the group.

On output, specifies the number of elements written to the buffer. If the buffer size is not sufficient, the function fails and this parameter receives the required length of the buffer.


### -param ProcessorIdleCycleTime [out]

The number of CPU clock cycles used by each idle thread. This buffer must be 8  times the number of processors in the system in size.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>



<a href="https://msdn.microsoft.com/4bf05e40-96d1-4c01-b3a8-8a45934b38c6">QueryIdleProcessorCycleTimeEx</a>



<a href="https://msdn.microsoft.com/1859bc0f-8065-4104-b421-1b4c020ad5ea">QueryProcessCycleTime</a>



<a href="https://msdn.microsoft.com/5828b073-48af-4118-9206-096b87c978e7">QueryThreadCycleTime</a>
 

 

