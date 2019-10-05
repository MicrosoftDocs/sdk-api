---
UID: NF:realtimeapiset.QueryInterruptTime
title: QueryInterruptTime function (realtimeapiset.h)
author: windows-sdk-content
description: Gets the current interrupt-time count.
old-location: base\queryinterrupttime.htm
tech.root: SysInfo
ms.assetid: FB2B179B-5E44-4201-86E2-DB386607FD90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryInterruptTime, QueryInterruptTime function, base.queryinterrupttime, realtimeapiset/QueryInterruptTime
ms.topic: function
f1_keywords: 
 - "realtimeapiset/QueryInterruptTime"
dev_langs:
 - c++
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
req.lib: Mincore.lib
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
 - QueryInterruptTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryInterruptTime function


## -description


Gets the current interrupt-time count. For a more precise count, use <a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise">QueryInterruptTimePrecise</a>.


## -parameters




### -param lpInterruptTime [out]

A pointer to a ULONGLONG in which to receive the interrupt-time count in system time units of 100 nanoseconds. Divide by ten million, or 1e7, to get seconds (there are 1e9 nanoseconds in a second, so there are 1e7 100-nanoseconds in a second).


## -returns



This function does not return a value.




## -remarks



The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick. The exact length of a clock tick depends on underlying hardware and can vary between systems.

Unlike system time, the interrupt-time count is not subject to adjustments by users or the Windows time service. Applications can use the interrupt-time count to measure finer durations than are possible with system time. Applications that require greater precision than the interrupt-time count should use a <a href="https://docs.microsoft.com/windows/desktop/winmsg/about-timers">high-resolution timer</a>. Use the <a href="https://docs.microsoft.com/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a> function to retrieve the frequency of the high-resolution timer and the <a href="https://docs.microsoft.com/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> function to retrieve the counter's value.

The  timer resolution set by the <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> and <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a> functions affects the resolution of  the <b>QueryInterruptTime</b> function. However, increasing the timer resolution is not recommended because it can reduce overall system performance and   increase system power consumption by preventing the processor from entering power-saving states. Instead, applications should use a high-resolution timer.

<div class="alert"><b>Note</b>  The <b>QueryInterruptTime</b> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time. The checked build is available to MSDN subscribers through the <a href="http://go.microsoft.com/fwlink/p/?linkid=8714">Microsoft Developer Network (MSDN)</a> Web site.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/interrupt-time">Interrupt Time</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise">QueryInterruptTimePrecise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise">QueryUnbiasedInterruptTimePrecise</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/system-power-states">System Power States</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/windows-time">Windows Time</a>
 

 

