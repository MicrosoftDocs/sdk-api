---
UID: NF:timezoneapi.SystemTimeToTzSpecificLocalTimeEx
title: SystemTimeToTzSpecificLocalTimeEx function (timezoneapi.h)
description: Converts a time in Coordinated Universal Time (UTC) with dynamic daylight saving time settings to a specified time zone's corresponding local time.
helpviewer_keywords: ["SystemTimeToTzSpecificLocalTimeEx","SystemTimeToTzSpecificLocalTimeEx function","base.systemtimetotzspecificlocaltimeex","timezoneapi/SystemTimeToTzSpecificLocalTimeEx"]
old-location: base\systemtimetotzspecificlocaltimeex.htm
tech.root: winprog
ms.assetid: A4483E33-6D74-4194-BF85-51FF55F1BF9A
ms.date: 12/05/2018
ms.keywords: SystemTimeToTzSpecificLocalTimeEx, SystemTimeToTzSpecificLocalTimeEx function, base.systemtimetotzspecificlocaltimeex, timezoneapi/SystemTimeToTzSpecificLocalTimeEx
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - SystemTimeToTzSpecificLocalTimeEx
 - timezoneapi/SystemTimeToTzSpecificLocalTimeEx
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
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - SystemTimeToTzSpecificLocalTimeEx
---

# SystemTimeToTzSpecificLocalTimeEx function


## -description

Converts a time in Coordinated Universal Time (UTC) with dynamic daylight saving time settings to a specified time zone's corresponding local time.

## -parameters

### -param lpTimeZoneInformation [in, optional]

A pointer to a <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure that specifies  the time zone and dynamic daylight saving time.

### -param lpUniversalTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the UTC time to be converted. The function converts this universal time to the specified time zone's corresponding local time.

### -param lpLocalTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the local time.

## -returns

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.