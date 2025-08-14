---
UID: NF:timezoneapi.GetTimeZoneInformation
title: GetTimeZoneInformation function (timezoneapi.h)
description: Retrieves the current time zone settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.
helpviewer_keywords: ["GetTimeZoneInformation","GetTimeZoneInformation function","_win32_gettimezoneinformation","base.gettimezoneinformation","timezoneapi/GetTimeZoneInformation"]
old-location: base\gettimezoneinformation.htm
tech.root: winprog
ms.assetid: 3d7601a5-6d22-4b1a-a222-9db46d21a3c7
ms.date: 12/05/2018
ms.keywords: GetTimeZoneInformation, GetTimeZoneInformation function, _win32_gettimezoneinformation, base.gettimezoneinformation, timezoneapi/GetTimeZoneInformation
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
 - GetTimeZoneInformation
 - timezoneapi/GetTimeZoneInformation
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
 - GetTimeZoneInformation
---

# GetTimeZoneInformation function


## -description

Retrieves the current time zone settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.

To support boundaries for daylight saving time that change from year to year, use the <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a>  or <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear">GetTimeZoneInformationForYear</a> function.

## -parameters

### -param lpTimeZoneInformation [out]

A pointer to a 
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure to receive the current settings.

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
Daylight saving time is not used in the current time zone, because there are no transition dates or automatic adjustment for daylight saving time is disabled.

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
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure. 



							

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
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure.

</td>
</tr>
</table>
 

If the function fails for other reasons, such as an out of memory error, it returns TIME_ZONE_ID_INVALID. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All translations between UTC time and local time are based on the following formula:

UTC = local time + bias

The bias is the difference, in minutes, between UTC time and local time.

 The <b>StandardName</b> and <b>DaylightName</b> members  of the resultant <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>  structure are localized according to the current user default UI language.


#### Examples

For an example, see <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-settimezoneinformation">SetTimeZoneInformation</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear">GetTimeZoneInformationForYear</a>



<a href="/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-settimezoneinformation">SetTimeZoneInformation</a>



<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>