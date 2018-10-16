---
UID: NF:timezoneapi.SystemTimeToTzSpecificLocalTime
title: SystemTimeToTzSpecificLocalTime function
author: windows-sdk-content
description: Converts a time in Coordinated Universal Time (UTC) to a specified time zone's corresponding local time.
old-location: base\systemtimetotzspecificlocaltime.htm
tech.root: sysinfo
ms.assetid: f3a87ec2-67a0-418f-af6e-6c0b5547cffb
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: SystemTimeToTzSpecificLocalTime, SystemTimeToTzSpecificLocalTime function, _win32_systemtimetotzspecificlocaltime, base.systemtimetotzspecificlocaltime, timezoneapi/SystemTimeToTzSpecificLocalTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SystemTimeToTzSpecificLocalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SystemTimeToTzSpecificLocalTime function


## -description


Converts a time in Coordinated Universal Time (UTC) to a specified time zone's corresponding local time.


## -parameters




### -param lpTimeZoneInformation

TBD


### -param lpUniversalTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that specifies the UTC time to be converted. The function converts this universal time to the specified time zone's corresponding local time.


### -param lpLocalTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the local time.


#### - lpTimeZone [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure that specifies the time zone of interest. 




If <i>lpTimeZone</i> is <b>NULL</b>, the function uses the currently active time zone.


## -returns



If the function succeeds, the return value is nonzero, and the function sets the members of the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure pointed to by <i>lpLocalTime</i> to the appropriate local time values.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SystemTimeToTzSpecificLocalTime</b> function takes into account whether daylight saving time (DST) is in effect for the local time to which the system time is to be converted.

The <b>SystemTimeToTzSpecificLocalTime</b> function may calculate the local time incorrectly under the following conditions:

<ul>
<li>The time zone uses a different UTC offset for the old and new years. </li>
<li>The UTC time to be converted and the calculated local time are in different years. </li>
</ul>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/54509a35-fa6a-4ee6-90f8-36c9ef55e1bc">Retrieving the Last-Write Time</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/3d7601a5-6d22-4b1a-a222-9db46d21a3c7">GetTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>



<a href="https://msdn.microsoft.com/d671499a-027d-4b1f-ae16-8b1978eb9783">TzSpecificLocalTimeToSystemTime</a>
 

 

