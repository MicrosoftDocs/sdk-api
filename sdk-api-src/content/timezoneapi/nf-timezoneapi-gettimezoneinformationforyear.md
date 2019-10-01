---
UID: NF:timezoneapi.GetTimeZoneInformationForYear
title: GetTimeZoneInformationForYear function (timezoneapi.h)
author: windows-sdk-content
description: Retrieves the time zone settings for the specified year and time zone. These settings control the translations between Coordinated Universal Time (UTC) and local time.
old-location: base\gettimezoneinformationforyear.htm
tech.root: SysInfo
ms.assetid: 5bd29a25-98f0-439e-be88-8011bbf98926
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTimeZoneInformationForYear, GetTimeZoneInformationForYear function, base.gettimezoneinformationforyear, timezoneapi/GetTimeZoneInformationForYear
ms.topic: function
f1_keywords:
- timezoneapi/GetTimeZoneInformationForYear
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- GetTimeZoneInformationForYear
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTimeZoneInformationForYear function


## -description


Retrieves the time zone settings for the specified year and time zone. These settings control the translations between Coordinated Universal Time (UTC) and local time.


## -parameters




### -param wYear [in]

The year for which the time zone settings are to be retrieved. The <i>wYear</i> parameter must be a local time value.


### -param pdtzi [in, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure that specifies the time zone.  To populate this parameter, call <a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation">EnumDynamicTimeZoneInformation</a> with the index of the time zone you want. If this parameter is <b>NULL</b>, the current time zone is used.


### -param ptzi [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that receives the time zone settings.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <i>wYear</i> parameter is assumed to be a local time value. If the local time is close to the transition between the old year and the new year (00:00:00 January 1), passing a UTC year to the <b>GetTimeZoneInformationForYear</b> function can cause the function to return time zone settings for the wrong year. 

 The <b>StandardName</b> and <b>DaylightName</b> members  of the resultant <a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>  structure are localized according to the current user default UI language.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>
 

 

