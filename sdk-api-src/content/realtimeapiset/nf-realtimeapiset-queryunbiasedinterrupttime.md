---
UID: NF:realtimeapiset.QueryUnbiasedInterruptTime
title: QueryUnbiasedInterruptTime function (realtimeapiset.h)
description: Gets the current unbiased interrupt-time count, in units of 100 nanoseconds. The unbiased interrupt-time count does not include time the system spends in sleep or hibernation.
helpviewer_keywords: ["QueryUnbiasedInterruptTime","QueryUnbiasedInterruptTime function","base.queryunbiasedinterrupttime","realtimeapiset/QueryUnbiasedInterruptTime"]
old-location: base\queryunbiasedinterrupttime.htm
tech.root: winprog
ms.assetid: f9cf5440-9be9-4ff9-b85c-2779b847954c
ms.date: 09/26/2024
ms.keywords: QueryUnbiasedInterruptTime, QueryUnbiasedInterruptTime function, base.queryunbiasedinterrupttime, realtimeapiset/QueryUnbiasedInterruptTime
req.header: realtimeapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - QueryUnbiasedInterruptTime
 - realtimeapiset/QueryUnbiasedInterruptTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-realtime-l1-1-2.dll
 - kernel32.dll
 - API-MS-Win-Core-realtime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-RealTime-l1-1-1.dll
api_name:
 - QueryUnbiasedInterruptTime
---

# QueryUnbiasedInterruptTime function


## -description

Gets the current unbiased interrupt-time count, in units of 100 nanoseconds. The unbiased interrupt-time count does not include time the system spends in sleep or hibernation.

## -parameters

### -param UnbiasedTime

TBD




#### - lpUnbiasedInterruptTime [out]

A pointer to a ULONGLONG in which to receive the unbiased interrupt-time count in system time units of 100 nanoseconds. Divide by ten million, or 1e7, to get seconds (there are 1e9 nanoseconds in a second, so there are 1e7 100-nanoseconds in a second).

## -returns

If the function succeeds, the return value is nonzero. If the function fails because it is called with a null parameter, the return value is zero.

## -remarks

The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick. The exact length of a clock tick depends on underlying hardware and can vary between systems.

The interrupt-time count retrieved by the <b>QueryUnbiasedInterruptTime</b> function reflects only the time that the system is in the working state. Therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation. The system uses biased interrupt time for some operations, such as ensuring that relative timers that would have expired during sleep expire immediately upon waking.

Unlike system time, the interrupt-time count is not subject to adjustments by users or the Windows time service. Applications can use the interrupt-time count to measure finer durations than are possible with system time. Applications that require greater precision than the interrupt-time count should use a <a href="/windows/desktop/winmsg/about-timers">high-resolution timer</a>. Use the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a> function to retrieve the frequency of the high-resolution timer and the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> function to retrieve the counter's value.

The  timer resolution set by the <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> and <a href="/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a> functions affects the resolution of  the <b>QueryUnbiasedInterruptTime</b> function. However, increasing the timer resolution is not recommended because it can reduce overall system performance and   increase system power consumption by preventing the processor from entering power-saving states. Instead, applications should use a high-resolution timer.

<div class="alert"><b>Note</b>  The <b>QueryUnbiasedInterruptTime</b> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/SysInfo/interrupt-time">Interrupt Time</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise">QueryInterruptTimePrecise</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise">QueryUnbiasedInterruptTimePrecise</a>



<a href="/windows/desktop/Power/system-power-states">System Power States</a>



<a href="/windows/desktop/SysInfo/windows-time">Windows Time</a>