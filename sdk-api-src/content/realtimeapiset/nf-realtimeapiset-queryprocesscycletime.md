---
UID: NF:realtimeapiset.QueryProcessCycleTime
title: QueryProcessCycleTime function (realtimeapiset.h)
author: windows-sdk-content
description: Retrieves the sum of the cycle time of all threads of the specified process.
old-location: base\queryprocesscycletime.htm
tech.root: ProcThread
ms.assetid: 1859bc0f-8065-4104-b421-1b4c020ad5ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryProcessCycleTime, QueryProcessCycleTime function, base.queryprocesscycletime, realtimeapiset/QueryProcessCycleTime, winbase/QueryProcessCycleTime
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
 - QueryProcessCycleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryProcessCycleTime function


## -description


Retrieves the sum of the cycle time of all threads of the specified process.


## -parameters




### -param ProcessHandle [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param CycleTime [out]

The number of CPU clock cycles used by the threads of the process. This value includes cycles spent in both user mode and kernel mode.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To enumerate the processes in the system, use the 
<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/75a5c4cf-ccc7-47ab-a2a9-88051e0a7d06">QueryIdleProcessorCycleTime</a>



<a href="https://msdn.microsoft.com/5828b073-48af-4118-9206-096b87c978e7">QueryThreadCycleTime</a>
 

 

