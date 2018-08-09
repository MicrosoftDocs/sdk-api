---
UID: NF:realtimeapiset.QueryInterruptTime
title: QueryInterruptTime function
author: windows-sdk-content
description: Gets the current interrupt-time count.
old-location: base\queryinterrupttime.htm
old-project: SysInfo
ms.assetid: FB2B179B-5E44-4201-86E2-DB386607FD90
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: QueryInterruptTime, QueryInterruptTime function, base.queryinterrupttime, realtimeapiset/QueryInterruptTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: realtimeapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
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
 - QueryInterruptTime
product: Windows
targetos: Windows
req.lib: Mincore.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# QueryInterruptTime function


## -description


Gets the current interrupt-time count. For a more precise count, use <a href="https://msdn.microsoft.com/0F65A707-0899-4F79-B7CD-16C9143C4173">QueryInterruptTimePrecise</a>.


## -parameters




### -param lpInterruptTime [out]

A pointer to a ULONGLONG in which to receive the interrupt-time count in system time units of 100 nanoseconds. Divide by ten million, or 1e7, to get seconds (there are 1e9 nanoseconds in a second, so there are 1e7 100-nanoseconds in a second).


## -returns



This function does not return a value.




## -remarks



The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick. The exact length of a clock tick depends on underlying hardware and can vary between systems.

Unlike system time, the interrupt-time count is not subject to adjustments by users or the Windows time service. Applications can use the interrupt-time count to measure finer durations than are possible with system time. Applications that require greater precision than the interrupt-time count should use a <a href="_win32_about_timers_cpp">high-resolution timer</a>. Use the <a href="https://msdn.microsoft.com/en-us/library/ms644905(v=VS.85).aspx">QueryPerformanceFrequency</a> function to retrieve the frequency of the high-resolution timer and the <a href="https://msdn.microsoft.com/en-us/library/ms644904(v=VS.85).aspx">QueryPerformanceCounter</a> function to retrieve the counter's value.

The  timer resolution set by the <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> and <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a> functions affects the resolution of  the <b>QueryInterruptTime</b> function. However, increasing the timer resolution is not recommended because it can reduce overall system performance and   increase system power consumption by preventing the processor from entering power-saving states. Instead, applications should use a high-resolution timer.

<div class="alert"><b>Note</b>  The <b>QueryInterruptTime</b> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time. The checked build is available to MSDN subscribers through the <a href="http://go.microsoft.com/fwlink/p/?linkid=8714">Microsoft Developer Network (MSDN)</a> Web site.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/56fe322e-53ea-4186-9b5e-352f69b09109">Interrupt Time</a>



<a href="https://msdn.microsoft.com/0F65A707-0899-4F79-B7CD-16C9143C4173">QueryInterruptTimePrecise</a>



<a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a>



<a href="https://msdn.microsoft.com/FADFC168-A3CF-4676-9B6E-7A4028049423">QueryUnbiasedInterruptTimePrecise</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564571">System Power States</a>



<a href="https://msdn.microsoft.com/95c00204-bfdf-4376-9aae-8d8139ba6750">Windows Time</a>
 

 

