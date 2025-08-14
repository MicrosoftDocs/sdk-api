---
UID: NF:timezoneapi.GetDynamicTimeZoneInformation
title: GetDynamicTimeZoneInformation function (timezoneapi.h)
description: Retrieves the current time zone and dynamic daylight saving time settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.
helpviewer_keywords: ["GetDynamicTimeZoneInformation","GetDynamicTimeZoneInformation function","base.getdynamictimezoneinformation","timezoneapi/GetDynamicTimeZoneInformation"]
old-location: base\getdynamictimezoneinformation.htm
tech.root: winprog
ms.assetid: 9f96f779-7e4f-4a50-a9dc-f3bc86c76ece
ms.date: 12/05/2018
ms.keywords: GetDynamicTimeZoneInformation, GetDynamicTimeZoneInformation function, base.getdynamictimezoneinformation, timezoneapi/GetDynamicTimeZoneInformation
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDynamicTimeZoneInformation
 - timezoneapi/GetDynamicTimeZoneInformation
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
 - GetDynamicTimeZoneInformation
---

# GetDynamicTimeZoneInformation function


## -description

Retrieves the current time zone and dynamic daylight saving time settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.

## -parameters

### -param pTimeZoneInformation [out]

A pointer to a <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.

## -returns

If the function succeeds, it returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Daylight saving time is not used in the current time zone, because there are no transition dates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_STANDARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The system is operating in the range covered by the <b>StandardDate</b> member of the 
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure. 



							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_DAYLIGHT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The system is operating in the range covered by the <b>DaylightDate</b> member of the 
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.

</td>
</tr>
</table>
 

If the function fails, it returns TIME_ZONE_ID_INVALID. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

 The <b>StandardName</b> and <b>DaylightName</b> members  of the resultant <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a>  structure are localized according to the current user default UI language.

## -see-also

<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>