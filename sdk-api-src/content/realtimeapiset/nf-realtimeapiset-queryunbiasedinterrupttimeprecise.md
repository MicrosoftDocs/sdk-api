---
UID: NF:realtimeapiset.QueryUnbiasedInterruptTimePrecise
title: QueryUnbiasedInterruptTimePrecise function
author: windows-sdk-content
description: Gets the current unbiased interrupt-time count, in a more precise form than QueryUnbiasedInterruptTime does. The unbiased interrupt-time count does not include time the system spends in sleep or hibernation.
old-location: base\queryunbiasedinterrupttimeprecise.htm
old-project: SysInfo
ms.assetid: FADFC168-A3CF-4676-9B6E-7A4028049423
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: QueryUnbiasedInterruptTimePrecise, QueryUnbiasedInterruptTimePrecise function, base.queryunbiasedinterrupttimeprecise, realtimeapiset/QueryUnbiasedInterruptTimePrecise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: realtimeapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
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
 - QueryUnbiasedInterruptTimePrecise
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# QueryUnbiasedInterruptTimePrecise function


## -description


Gets the current unbiased interrupt-time count, in a more precise form than <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> does. The unbiased interrupt-time count does not include time the system spends in sleep or hibernation. 


## -parameters




### -param lpUnbiasedInterruptTimePrecise [out]

A pointer to a ULONGLONG in which to receive the unbiased interrupt-time count in system time units of 100 nanoseconds. Divide by ten million, or 1e7, to get seconds (there are 1e9 nanoseconds in a second, so there are 1e7 100-nanoseconds in a second).


## -returns



This function does not return a value.




## -remarks



<b>QueryUnbiasedInterruptTimePrecise</b> is similar to the <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> routine, but is more precise. The interrupt time reported by <b>QueryUnbiasedInterruptTime</b> is based on the latest tick of the system clock timer. The system clock timer is the hardware timer that periodically generates interrupts for the system clock. The uniform period between system clock timer interrupts is referred to as a system clock tick, and is typically in the range of 0.5 milliseconds to 15.625 milliseconds, depending on the hardware platform. The interrupt time value retrieved by <b>QueryUnbiasedInterruptTime</b> is accurate within a system clock tick.

To provide a system time value that is more precise than that of <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a>, <b>QueryUnbiasedInterruptTimePrecise</b> reads the timer hardware directly,  therefore a <b>QueryUnbiasedInterruptTimePrecise</b> call can be slower than a <b>QueryUnbiasedInterruptTime</b> call.

Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553075">KeQueryTimeIncrement</a> routine to determine the duration of a system clock tick.


				Also see Remarks in <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a>.

<div class="alert"><b>Note</b>  
				The <b>QueryUnbiasedInterruptTimePrecise</b> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time. The checked build is available to MSDN subscribers through the <a href="http://go.microsoft.com/fwlink/p/?linkid=8714">Microsoft Developer Network (MSDN)</a> Web site.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see
				<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/56fe322e-53ea-4186-9b5e-352f69b09109">Interrupt Time</a>



<a href="https://msdn.microsoft.com/FB2B179B-5E44-4201-86E2-DB386607FD90">QueryInterruptTime</a>



<a href="https://msdn.microsoft.com/0F65A707-0899-4F79-B7CD-16C9143C4173">QueryInterruptTimePrecise</a>



<a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564571">System Power States</a>



<a href="https://msdn.microsoft.com/95c00204-bfdf-4376-9aae-8d8139ba6750">Windows Time</a>
 

 

