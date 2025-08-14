---
UID: NF:timezoneapi.SystemTimeToTzSpecificLocalTime
title: SystemTimeToTzSpecificLocalTime function (timezoneapi.h)
description: Converts a time in Coordinated Universal Time (UTC) to a specified time zone's corresponding local time.
helpviewer_keywords: ["SystemTimeToTzSpecificLocalTime","SystemTimeToTzSpecificLocalTime function","_win32_systemtimetotzspecificlocaltime","base.systemtimetotzspecificlocaltime","timezoneapi/SystemTimeToTzSpecificLocalTime"]
old-location: base\systemtimetotzspecificlocaltime.htm
tech.root: winprog
ms.assetid: f3a87ec2-67a0-418f-af6e-6c0b5547cffb
ms.date: 12/05/2018
ms.keywords: SystemTimeToTzSpecificLocalTime, SystemTimeToTzSpecificLocalTime function, _win32_systemtimetotzspecificlocaltime, base.systemtimetotzspecificlocaltime, timezoneapi/SystemTimeToTzSpecificLocalTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SystemTimeToTzSpecificLocalTime
 - timezoneapi/SystemTimeToTzSpecificLocalTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-timezone-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SystemTimeToTzSpecificLocalTime
---

# SystemTimeToTzSpecificLocalTime function


## -description

Converts a time in Coordinated Universal Time (UTC) to a specified time zone's corresponding local time.

## -parameters

### -param lpTimeZoneInformation [in, optional]

A pointer to a 
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that specifies the time zone of interest. 




If <i>lpTimeZone</i> is <b>NULL</b>, the function uses the currently active time zone.

### -param lpUniversalTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the UTC time to be converted. The function converts this universal time to the specified time zone's corresponding local time.

### -param lpLocalTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the local time.

## -returns

If the function succeeds, the return value is nonzero, and the function sets the members of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure pointed to by <i>lpLocalTime</i> to the appropriate local time values.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SystemTimeToTzSpecificLocalTime</b> function takes into account whether daylight saving time (DST) is in effect for the local time to which the system time is to be converted.

The <b>SystemTimeToTzSpecificLocalTime</b> function may calculate the local time incorrectly under the following conditions:

<ul>
<li>The time zone uses a different UTC offset for the old and new years. </li>
<li>The UTC time to be converted and the calculated local time are in different years. </li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/SysInfo/retrieving-the-last-write-time">Retrieving the Last-Write Time</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation">GetTimeZoneInformation</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime">TzSpecificLocalTimeToSystemTime</a>