---
UID: NF:sysinfoapi.SetSystemTimeAdjustment
title: SetSystemTimeAdjustment function
author: windows-sdk-content
description: Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information.
old-location: base\setsystemtimeadjustment.htm
tech.root: SysInfo
ms.assetid: 93c72511-057c-4b26-a4ae-1d225a80c572
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: SetSystemTimeAdjustment, SetSystemTimeAdjustment function, _win32_setsystemtimeadjustment, base.setsystemtimeadjustment, sysinfoapi/SetSystemTimeAdjustment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetSystemTimeAdjustment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSystemTimeAdjustment function


## -description


Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information. 


## -parameters




### -param dwTimeAdjustment [in]

This value represents the number of 100-nanosecond units added to the system time-of-day  for each <i>lpTimeIncrement</i> period of time that actually passes. Call <a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a> to obtain the <i>lpTimeIncrement</i> value. See remarks.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. One way the function can fail is if the caller does not possess the SE_SYSTEMTIME_NAME privilege.




## -remarks



The 
<a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a> and 
<b>SetSystemTimeAdjustment</b> functions support algorithms that synchronize the time-of-day clock, reported via 
<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a> and 
<a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a>, with another time source using a periodic time adjustment.

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
For this mode, <i>bTimeAdjustmentDisabled</i> is set to <b>FALSE</b>. For each <i>lpTimeIncrement</i> period of time that actually passes, <i>dwTimeAdjustment</i> will be added to the time of day. The period of time represented by <i>lpTimeIncrement</i> can be determined by calling <a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a>. The <i>lpTimeIncrement</i> value is fixed by the system upon start and does not change during system operation and is completely independent of the system’s internal clock interrupt resolution at any given time. Given this, the <i>lpTimeIncrement</i> value simply expresses a period of time for which <i>dwTimeAdjustment</i> will be applied to the system’s time-of-day clock.

If the <i>dwTimeAdjustment</i> value is smaller than <i>lpTimeIncrement</i>, the time-of-day clock will advance at a rate slower than normal. If the <i>dwTimeAdjustment</i> value is larger than <i>lpTimeIncrement</i>, the time-of-day clock will advance at a rate faster than normal. The degree to which the time-of-day-clock will run faster or slower depends on how far the <i>dwTimeAdjustment</i> value is above or below the <i>lpTimeIncrement</i> value.  If <i>dwTimeAdjustment</i> equals <i>lpTimeIncrement</i>, the time-of-day clock will advance at normal speed. 

</td>
</tr>
</table>
 

An application must have system-time privilege (the SE_SYSTEMTIME_NAME privilege) for this function to succeed. The SE_SYSTEMTIME_NAME privilege is disabled by default. Use the 
<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function to enable the privilege before calling 
<b>SetSystemTimeAdjustment</b>, and then to disable the privilege after the 
<b>SetSystemTimeAdjustment</b> call. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a>



<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

