---
UID: NF:realtimeapiset.QueryInterruptTimePrecise
title: QueryInterruptTimePrecise function (realtimeapiset.h)
description: Gets the current interrupt-time count, in a more precise form than QueryInterruptTime does.
helpviewer_keywords: ["QueryInterruptTimePrecise","QueryInterruptTimePrecise function","base.queryinterrupttimeprecise","realtimeapiset/QueryInterruptTimePrecise"]
old-location: base\queryinterrupttimeprecise.htm
tech.root: winprog
ms.assetid: 0F65A707-0899-4F79-B7CD-16C9143C4173
ms.date: 12/05/2018
ms.keywords: QueryInterruptTimePrecise, QueryInterruptTimePrecise function, base.queryinterrupttimeprecise, realtimeapiset/QueryInterruptTimePrecise
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryInterruptTimePrecise
 - realtimeapiset/QueryInterruptTimePrecise
dev_langs:
 - c++
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
 - QueryInterruptTimePrecise
---

# QueryInterruptTimePrecise function


## -description

Gets the current interrupt-time count, in a more precise form than <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a> does.

## -parameters

### -param lpInterruptTimePrecise [out]

A pointer to a ULONGLONG in which to receive the interrupt-time count in system time units of 100 nanoseconds. Divide by ten million, or 1e7, to get seconds (there are 1e9 nanoseconds in a second, so there are 1e7 100-nanoseconds in a second).

## -remarks

<b>QueryInterruptTimePrecise</b> is similar to the <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a> routine, but is more precise. The interrupt time reported by <b>QueryInterruptTime</b> is based on the latest tick of the system clock timer. The system clock timer is the hardware timer that periodically generates interrupts for the system clock. The uniform period between system clock timer interrupts is referred to as a system clock tick, and is typically in the range of 0.5 milliseconds to 15.625 milliseconds, depending on the hardware platform. The interrupt time value retrieved by <b>QueryInterruptTime</b> is accurate within a system clock tick.

To provide a system time value that is more precise than that of <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a>, <b>QueryInterruptTimePrecise</b> reads the timer hardware directly,  therefore a <b>QueryInterruptTimePrecise</b> call can be slower than a <b>QueryInterruptTime</b> call.

Call the <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerytimeincrement">KeQueryTimeIncrement</a> routine to determine the duration of a system clock tick.

Also see Remarks in <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a>.

<div class="alert"><b>Note</b>  The <b>QueryInterruptTimePrecise</b> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0601 or later. For more information, see
                <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/SysInfo/interrupt-time">Interrupt Time</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime">QueryInterruptTime</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime">QueryUnbiasedInterruptTime</a>



<a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise">QueryUnbiasedInterruptTimePrecise</a>



<a href="/windows/desktop/Power/system-power-states">System Power States</a>



<a href="/windows/desktop/SysInfo/windows-time">Windows Time</a>