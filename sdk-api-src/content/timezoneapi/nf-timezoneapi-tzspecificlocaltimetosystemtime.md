---
UID: NF:timezoneapi.TzSpecificLocalTimeToSystemTime
title: TzSpecificLocalTimeToSystemTime function (timezoneapi.h)
description: Converts the specified local time to the corresponding time in Coordinated Universal Time (UTC).
helpviewer_keywords: ["TzSpecificLocalTimeToSystemTime","TzSpecificLocalTimeToSystemTime function","_win32_tzspecificlocaltimetosystemtime","base.tzspecificlocaltimetosystemtime","timezoneapi/TzSpecificLocalTimeToSystemTime"]
old-location: base\tzspecificlocaltimetosystemtime.htm
tech.root: winprog
ms.assetid: d671499a-027d-4b1f-ae16-8b1978eb9783
ms.date: 12/16/2025
ms.keywords: TzSpecificLocalTimeToSystemTime, TzSpecificLocalTimeToSystemTime function, _win32_tzspecificlocaltimetosystemtime, base.tzspecificlocaltimetosystemtime, timezoneapi/TzSpecificLocalTimeToSystemTime
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
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - TzSpecificLocalTimeToSystemTime
 - timezoneapi/TzSpecificLocalTimeToSystemTime
dev_langs:
 - c++
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
---

# TzSpecificLocalTimeToSystemTime function

## -description

Converts the specified local time to the corresponding time in Coordinated Universal Time (UTC).

## -parameters

### -param lpTimeZoneInformation [in, optional]

A pointer to a <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that specifies the time zone for the time specified in *lpLocalTime*.

If *lpTimeZoneInformation* is **NULL**, the function uses the currently active time zone.

### -param lpLocalTime [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the local time to be converted. The function converts this time to the corresponding UTC time.

### -param lpUniversalTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the UTC time.

## -returns

If the function succeeds, the return value is nonzero, and the function sets the members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure pointed to by *lpUniversalTime* to the appropriate values.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

**TzSpecificLocalTimeToSystemTime** takes into account whether daylight saving time (DST) is in effect for the local time to be converted.

> [!IMPORTANT]
> The following local times, near DST transitions, can be **ambiguous** or **invalid** and might result in unexpected behavior (as there is no guaranteed "correct" result).
>
> - During the transition from daylight saving time to standard time, the local clock repeats. A local time within the repeated window is **ambiguous** because it occurs twice, once in daylight saving time and once in standard time.
> - During the transition from standard time to daylight saving time, the local clock jumps forward. A local time within the skipped window is **invalid** because it does not have a valid UTC conversion.
>
> If the specified local time is either ambiguous or invalid, the function treats it as daylight saving time and applies the daylight saving time bias. Applications requiring continuity or precision should avoid this function and use UTC time instead.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation">GetTimeZoneInformation</a>



<a href="/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime">SystemTimeToTzSpecificLocalTime</a>



<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>
