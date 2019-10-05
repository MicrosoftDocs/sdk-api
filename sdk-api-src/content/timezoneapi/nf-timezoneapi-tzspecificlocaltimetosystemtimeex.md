---
UID: NF:timezoneapi.TzSpecificLocalTimeToSystemTimeEx
title: TzSpecificLocalTimeToSystemTimeEx function (timezoneapi.h)
author: windows-sdk-content
description: Converts a local time to a time with dynamic daylight saving time settings to Coordinated Universal Time (UTC).
old-location: base\tzspecificlocaltimetosystemtimeex.htm
tech.root: SysInfo
ms.assetid: C202F91E-FFFF-412D-A968-3B7AE60A5846
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TzSpecificLocalTimeToSystemTimeEx, TzSpecificLocalTimeToSystemTimeEx function, base.tzspecificlocaltimetosystemtimeex, timezoneapi/TzSpecificLocalTimeToSystemTimeEx
ms.topic: function
f1_keywords: 
 - "timezoneapi/TzSpecificLocalTimeToSystemTimeEx"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - TzSpecificLocalTimeToSystemTimeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TzSpecificLocalTimeToSystemTimeEx function


## -description


Converts a local time to a time with dynamic daylight saving time settings  to Coordinated Universal Time (UTC).


## -parameters




### -param lpTimeZoneInformation [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure that specifies  the time zone and dynamic daylight saving time.


### -param lpLocalTime [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that specifies the local time to be converted. The function converts this time to the corresponding UTC time.


### -param lpUniversalTime [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the UTC time.


## -returns



If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



