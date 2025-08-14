---
UID: NF:sysinfoapi.SetSystemTimeAdjustment
title: SetSystemTimeAdjustment function (sysinfoapi.h)
description: Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information. (SetSystemTimeAdjustment)
helpviewer_keywords: ["SetSystemTimeAdjustment","SetSystemTimeAdjustment function","_win32_setsystemtimeadjustment","base.setsystemtimeadjustment","sysinfoapi/SetSystemTimeAdjustment"]
old-location: base\setsystemtimeadjustment.htm
tech.root: winprog
ms.assetid: 93c72511-057c-4b26-a4ae-1d225a80c572
ms.date: 12/05/2018
ms.keywords: SetSystemTimeAdjustment, SetSystemTimeAdjustment function, _win32_setsystemtimeadjustment, base.setsystemtimeadjustment, sysinfoapi/SetSystemTimeAdjustment
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
 - SetSystemTimeAdjustment
 - sysinfoapi/SetSystemTimeAdjustment
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
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetSystemTimeAdjustment
---

# SetSystemTimeAdjustment function


## -description

Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information.

## -parameters

### -param dwTimeAdjustment [in]

This value represents the number of 100-nanosecond units added to the system time-of-day  for each <i>lpTimeIncrement</i> period of time that actually passes. Call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a> to obtain the <i>lpTimeIncrement</i> value. See remarks.

<div class="alert"><b>Note</b>  <p class="note">Currently, Windows Vista and Windows 7 machines will lose any time adjustments set less than 16. 

</div>
<div> </div>

### -param bTimeAdjustmentDisabled [in]

The time adjustment mode that the system is to use. Periodic system time adjustments can be disabled or enabled. 




A value of <b>TRUE</b> specifies that periodic time adjustment is to be disabled. When disabled, the value of <i>dwTimeAdjustment</i> is ignored, and the system may adjust the time of day using its own internal time synchronization mechanisms. These internal time synchronization mechanisms may cause the time-of-day clock to change during the normal course of the system operation, which can include noticeable jumps in time as deemed necessary by the system.

A value of <b>FALSE</b> specifies that periodic time adjustment is to be enabled, and will be used to adjust the time-of-day clock. The system will not interfere with the time adjustment scheme, and will not attempt to synchronize time of day on its own.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One way the function can fail is if the caller does not possess the SE_SYSTEMTIME_NAME privilege.

## -remarks

The 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a> and 
<b>SetSystemTimeAdjustment</b> functions support algorithms that synchronize the time-of-day clock, reported via 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a> and 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>, with another time source using a periodic time adjustment.

The 
<b>SetSystemTimeAdjustment</b> function supports two modes of time synchronization:

<table>
<tr>
<th>Mode</th>
<th>Behavior</th>
</tr>
<tr>
<td>
Time-Adjustment Disabled

</td>
<td>
For this mode, <i>bTimeAdjustmentDisabled</i> is set to <b>TRUE</b>. In this mode, the value of <i>dwTimeAdjustment</i> is ignored, and the system may adjust the time of day using its own internal time synchronization mechanisms. These internal time synchronization mechanisms may cause the time-of-day clock to change during the normal course of the system operation, which can include noticeable jumps in time as deemed necessary by the system.

</td>
</tr>
<tr>
<td>
Time-Adjustment Enabled

</td>
<td>
For this mode, <i>bTimeAdjustmentDisabled</i> is set to <b>FALSE</b>. For each <i>lpTimeIncrement</i> period of time that actually passes, <i>dwTimeAdjustment</i> will be added to the time of day. The period of time represented by <i>lpTimeIncrement</i> can be determined by calling <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a>. The <i>lpTimeIncrement</i> value is fixed by the system upon start and does not change during system operation and is completely independent of the system’s internal clock interrupt resolution at any given time. Given this, the <i>lpTimeIncrement</i> value simply expresses a period of time for which <i>dwTimeAdjustment</i> will be applied to the system’s time-of-day clock.

If the <i>dwTimeAdjustment</i> value is smaller than <i>lpTimeIncrement</i>, the time-of-day clock will advance at a rate slower than normal. If the <i>dwTimeAdjustment</i> value is larger than <i>lpTimeIncrement</i>, the time-of-day clock will advance at a rate faster than normal. The degree to which the time-of-day-clock will run faster or slower depends on how far the <i>dwTimeAdjustment</i> value is above or below the <i>lpTimeIncrement</i> value.  If <i>dwTimeAdjustment</i> equals <i>lpTimeIncrement</i>, the time-of-day clock will advance at normal speed. 

</td>
</tr>
</table>
 

An application must have system-time privilege (the SE_SYSTEMTIME_NAME privilege) for this function to succeed. The SE_SYSTEMTIME_NAME privilege is disabled by default. Use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to enable the privilege before calling 
<b>SetSystemTimeAdjustment</b>, and then to disable the privilege after the 
<b>SetSystemTimeAdjustment</b> call. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>
