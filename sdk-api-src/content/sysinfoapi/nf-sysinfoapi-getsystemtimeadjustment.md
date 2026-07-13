---
UID: NF:sysinfoapi.GetSystemTimeAdjustment
title: GetSystemTimeAdjustment function (sysinfoapi.h)
description: Determines whether the system is applying periodic time adjustments to its time-of-day clock, and obtains the value and period of any such adjustments.
helpviewer_keywords: ["GetSystemTimeAdjustment","GetSystemTimeAdjustment function","_win32_getsystemtimeadjustment","base.getsystemtimeadjustment","sysinfoapi/GetSystemTimeAdjustment"]
old-location: base\getsystemtimeadjustment.htm
tech.root: winprog
ms.assetid: 6c748726-c81d-4669-87a1-28aad0fccead
ms.date: 12/05/2018
ms.keywords: GetSystemTimeAdjustment, GetSystemTimeAdjustment function, _win32_getsystemtimeadjustment, base.getsystemtimeadjustment, sysinfoapi/GetSystemTimeAdjustment
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemTimeAdjustment
 - sysinfoapi/GetSystemTimeAdjustment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemTimeAdjustment
---

# GetSystemTimeAdjustment function


## -description

Determines whether the system is applying periodic time adjustments to its time-of-day clock, and obtains the value and period of any such adjustments.

## -parameters

### -param lpTimeAdjustment [out]

A pointer to a variable that the function sets to the number of <i>lpTimeIncrement</i> 100-nanosecond units added to the time-of-day clock for every  period of time which actually passes as counted by the system. This value only has meaning if <i>lpTimeAdjustmentDisabled</i> is <b>FALSE</b>.

### -param lpTimeIncrement [out]

A pointer to a variable that the function sets to the interval in 100-nanosecond units at which the system will add <i>lpTimeAdjustment</i> to the time-of-day clock. This value only has meaning if <i>lpTimeAdjustmentDisabled</i> is <b>FALSE</b>.

### -param lpTimeAdjustmentDisabled [out]

A pointer to a variable that the function sets to indicate whether periodic time adjustment is in effect. 




A value of <b>TRUE</b> indicates that periodic time adjustment is disabled, and the system time-of-day clock advances at the normal rate. In this mode, the system may adjust the time of day using its own internal time synchronization mechanisms. These internal time synchronization mechanisms may cause the time-of-day clock to change during the normal course of the system operation, which can include noticeable jumps in time as deemed necessary by the system.

A value of <b>FALSE</b> indicates that periodic time adjustment is being used to adjust the time-of-day clock. For each <i>lpTimeIncrement</i> period of time that actually passes, <i>lpTimeAdjustment</i> will be added to the time of day.  If the <i>lpTimeAdjustment</i> value is smaller than <i>lpTimeIncrement</i>, the system time-of-day clock will advance at a rate slower than normal. If the <i>lpTimeAdjustment</i> value is larger than <i>lpTimeIncrement</i>, the time-of-day clock will advance at a rate faster than normal. If <i>lpTimeAdjustment</i> equals <i>lpTimeIncrement</i>, the time-of-day clock will advance at its normal speed.  The <i>lpTimeAdjustment</i>  value can be set by calling <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a>. The <i>lpTimeIncrement</i> value is fixed by the system upon start, and does not change during system operation. In this mode, the system will not interfere with the time adjustment scheme, and will not attempt to synchronize time of day on its own via other techniques.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetSystemTimeAdjustment</b> and <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a> functions can be used to support algorithms that want to synchronize the time-of-day clock, reported by <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a> and <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>, with another time source by using a periodic time adjustment.

The <b>GetSystemTimeAdjustment</b> function lets a caller determine whether periodic time adjustment is enabled, and if it is, obtain the amount of each adjustment and the time between adjustments. The <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a> function lets a caller enable or disable periodic time adjustment, and set the value of the adjusting increment.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>