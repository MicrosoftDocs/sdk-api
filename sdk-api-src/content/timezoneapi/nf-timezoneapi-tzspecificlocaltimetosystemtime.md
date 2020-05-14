---
UID: NF:timezoneapi.TzSpecificLocalTimeToSystemTime
title: TzSpecificLocalTimeToSystemTime function (timezoneapi.h)
description: Converts a local time to a time in Coordinated Universal Time (UTC).helpviewer_keywords: ["TzSpecificLocalTimeToSystemTime","TzSpecificLocalTimeToSystemTime function","_win32_tzspecificlocaltimetosystemtime","base.tzspecificlocaltimetosystemtime","timezoneapi/TzSpecificLocalTimeToSystemTime"]
old-location: base\tzspecificlocaltimetosystemtime.htm
tech.root: SysInfo
ms.assetid: d671499a-027d-4b1f-ae16-8b1978eb9783
ms.date: 12/05/2018
ms.keywords: TzSpecificLocalTimeToSystemTime, TzSpecificLocalTimeToSystemTime function, _win32_tzspecificlocaltimetosystemtime, base.tzspecificlocaltimetosystemtime, timezoneapi/TzSpecificLocalTimeToSystemTime
f1_keywords:
- timezoneapi/TzSpecificLocalTimeToSystemTime
dev_langs:
- c++
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- TzSpecificLocalTimeToSystemTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TzSpecificLocalTimeToSystemTime function


## -description


Converts a local time to a time in Coordinated Universal Time (UTC).


## -parameters




### -param lpTimeZoneInformation [in, optional]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that specifies the time zone for the time specified in <i>lpLocalTime</i>.

If <i>lpTimeZoneInformation</i> is <b>NULL</b>, the function uses the currently active time zone.


### -param lpLocalTime [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the local time to be converted. The function converts this time to the corresponding UTC time.


### -param lpUniversalTime [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the UTC time.


## -returns



If the function succeeds, the return value is nonzero, and the function sets the members of the 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure pointed to by <i>lpUniversalTime</i> to the appropriate values.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<b>TzSpecificLocalTimeToSystemTime</b> takes into account whether daylight saving time (DST) is in effect for the local time to be converted.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation">GetTimeZoneInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime">SystemTimeToTzSpecificLocalTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>
 

 

