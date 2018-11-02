---
UID: NF:realtimeapiset.QueryIdleProcessorCycleTimeEx
title: QueryIdleProcessorCycleTimeEx function
author: windows-sdk-content
description: Retrieves the accumulated cycle time for the idle thread on each logical processor in the specified processor group.
old-location: base\queryidleprocessorcycletimeex.htm
tech.root: procthread
ms.assetid: 4bf05e40-96d1-4c01-b3a8-8a45934b38c6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: QueryIdleProcessorCycleTimeEx, QueryIdleProcessorCycleTimeEx function, base.queryidleprocessorcycletimeex, realtimeapiset/QueryIdleProcessorCycleTimeEx, winbase/QueryIdleProcessorCycleTimeEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: realtimeapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - kernel32.dll
 - API-MS-Win-Core-realtime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-RealTime-l1-1-1.dll
api_name:
 - QueryIdleProcessorCycleTimeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryIdleProcessorCycleTimeEx function


## -description


Retrieves the accumulated cycle time for the idle thread on each logical processor in the specified processor group. 


## -parameters




### -param Group [in]

The number of the processor group for which to retrieve the cycle time.


### -param BufferLength [in, out]

On input, specifies the size of the <i>ProcessorIdleCycleTime</i> buffer, in bytes. This buffer is expected to be 8 times the number of processors in the group. 

On output, specifies the number of elements written to the buffer. If the buffer size is not sufficient, the function fails and this parameter receives the required length of the buffer.


### -param ProcessorIdleCycleTime [out]

The number of CPU clock cycles used by each idle thread. If this parameter is NULL, the function updates the <i>BufferLength</i> parameter with the required length.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>



<a href="https://msdn.microsoft.com/75a5c4cf-ccc7-47ab-a2a9-88051e0a7d06">QueryIdleProcessorCycleTime</a>
 

 

