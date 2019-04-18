---
UID: NF:sysinfoapi.GetProcessorSystemCycleTime
title: GetProcessorSystemCycleTime function (sysinfoapi.h)
author: windows-sdk-content
description: Retrieves the cycle time each processor in the specified processor group spent executing deferred procedure calls (DPCs) and interrupt service routines (ISRs) since the processor became active.
old-location: base\getprocessorsystemcycletime.htm
tech.root: ProcThread
ms.assetid: 231c2a26-4a2e-4c66-a652-eb9c886369b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProcessorSystemCycleTime, GetProcessorSystemCycleTime function, base.getprocessorsystemcycletime, sysinfoapi/GetProcessorSystemCycleTime
ms.topic: function
req.header: sysinfoapi.h
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
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetProcessorSystemCycleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetProcessorSystemCycleTime function


## -description


Retrieves the cycle time each processor in the specified processor group spent executing deferred procedure calls (DPCs) and interrupt service routines (ISRs) since the processor became active.


## -parameters




### -param Group [in]

The number of the processor group for which to retrieve the cycle time.


### -param Buffer [out]

A pointer to a buffer to receive a SYSTEM_PROCESSOR_CYCLE_TIME_INFORMATION structure for each processor in the group. On output, the DWORD64 <b>CycleTime</b> member of this structure is set to the cycle time for one processor.


### -param ReturnedLength [in, out]

The size of the buffer, in bytes. When the function returns, this parameter contains the number of bytes written to <i>Buffer</i>. If the buffer is too small for the data, the function fails with ERROR_INSUFFICIENT_BUFFER and sets the <i>ReturnedLength</i> parameter to the required buffer size.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

If the error value is ERROR_INSUFFICIENT_BUFFER, the <i>ReturnedLength</i> parameter contains the required buffer size.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>
 

 

