---
UID: NF:realtimeapiset.QueryThreadCycleTime
title: QueryThreadCycleTime function
author: windows-sdk-content
description: Retrieves the cycle time for the specified thread.
old-location: base\querythreadcycletime.htm
tech.root: ProcThread
ms.assetid: 5828b073-48af-4118-9206-096b87c978e7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: QueryThreadCycleTime, QueryThreadCycleTime function, base.querythreadcycletime, realtimeapiset/QueryThreadCycleTime, winbase/QueryThreadCycleTime
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
 - QueryThreadCycleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryThreadCycleTime function


## -description


Retrieves the cycle time for the specified thread.


## -parameters




### -param ThreadHandle [in]

A handle to the thread. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param CycleTime [out]

The number of CPU clock cycles used by the thread. This value includes cycles spent in both user mode and kernel mode.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To enumerate the threads of the process, use the <a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a> and <a href="https://msdn.microsoft.com/5efe514e-626c-4138-97a0-bdad217c424f">Thread32Next</a> functions. To get the thread handle for a thread identifier, use the 
<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function.

Do not attempt to convert the CPU clock cycles returned by <b>QueryThreadCycleTime</b> to elapsed time. This function uses timer services provided by the CPU, which can vary in implementation. For example, some CPUs will vary the frequency of the timer when changing the frequency at which the CPU runs and others will leave it at a fixed rate. The behavior of each CPU is described in the documentation provided by the CPU vendor.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later.




## -see-also




<a href="https://msdn.microsoft.com/75a5c4cf-ccc7-47ab-a2a9-88051e0a7d06">QueryIdleProcessorCycleTime</a>



<a href="https://msdn.microsoft.com/1859bc0f-8065-4104-b421-1b4c020ad5ea">QueryProcessCycleTime</a>
 

 

