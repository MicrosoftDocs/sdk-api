---
UID: NS:timezoneapi._TIME_ZONE_INFORMATION
title: "_TIME_ZONE_INFORMATION"
author: windows-sdk-content
description: Specifies settings for a time zone.
old-location: base\time_zone_information_str.htm
tech.root: sysinfo
ms.assetid: 18c10ad6-8bc9-4a3b-a424-d17ee1d9e004
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPTIME_ZONE_INFORMATION, *PTIME_ZONE_INFORMATION, PTIME_ZONE_INFORMATION, PTIME_ZONE_INFORMATION structure pointer, TIME_ZONE_INFORMATION, TIME_ZONE_INFORMATION structure, _TIME_ZONE_INFORMATION, _TIME_ZONE_INFORMATION structure, _win32_time_zone_information_str, base.time_zone_information_str, timezoneapi/PTIME_ZONE_INFORMATION, timezoneapi/_TIME_ZONE_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - timezoneapi.h
api_name:
 - TIME_ZONE_INFORMATION
product: Windows
targetos: Windows
req.typenames: TIME_ZONE_INFORMATION, *PTIME_ZONE_INFORMATION, *LPTIME_ZONE_INFORMATION
req.redist: 
---

# _TIME_ZONE_INFORMATION structure


## -description


Specifies settings for a time zone.


## -struct-fields




### -field Bias

The current bias for local time translation on this computer, in minutes. The bias is the difference, in minutes, between Coordinated Universal Time (UTC) and local time. All translations between UTC and local time are based on the following formula: 




UTC = local time + bias

This member is required.


### -field StandardName

A description for standard time. For example, "EST" could indicate Eastern Standard Time. The string will be  returned unchanged by the 
<a href="https://msdn.microsoft.com/3d7601a5-6d22-4b1a-a222-9db46d21a3c7">GetTimeZoneInformation</a> function. This string can be empty.


### -field StandardDate

A 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains a date and local time when the transition from daylight saving time to standard time occurs on this operating system. If the time zone does not support daylight saving time or if the caller needs to disable daylight saving time, the <b>wMonth</b> member in the 
<b>SYSTEMTIME</b> structure must be zero. If this date is specified, the <b>DaylightDate</b> member of this structure must also be specified. 


Otherwise, the system assumes the time zone data is invalid and no changes will be applied.

To select the correct day in the month, set the <b>wYear</b> member to zero, the <b>wHour</b> and <b>wMinute</b> members to the transition time, the <b>wDayOfWeek</b> member to the appropriate weekday, and the <b>wDay</b> member to indicate the occurrence of the day of the week within the month (1 to 5, where 5 indicates the final occurrence during the month if that day of the week does not occur 5 times).

Using this notation, specify 02:00 on the first Sunday in April as follows: <b>wHour</b> = 2, <b>wMonth</b> = 4, <b>wDayOfWeek</b> = 0, <b>wDay</b> = 1. Specify 02:00 on the last Thursday in October as follows: <b>wHour</b> = 2, <b>wMonth</b> = 10, <b>wDayOfWeek</b> = 4, <b>wDay</b> = 5.

If the <b>wYear</b> member is not zero, the transition date is absolute; it will only occur one time. Otherwise, it is a relative date that occurs yearly.


### -field StandardBias

The bias value to be used during local time translations that occur during standard time. This member is ignored if a value for the <b>StandardDate</b> member is not supplied. 




This value is added to the value of the <b>Bias</b> member to form the bias used during standard time. In most time zones, the value of this member is zero.


### -field DaylightName

A description for daylight saving time. For example, "PDT" could indicate Pacific Daylight Time. The string will be  returned unchanged by the 
<a href="https://msdn.microsoft.com/3d7601a5-6d22-4b1a-a222-9db46d21a3c7">GetTimeZoneInformation</a> function. This string can be empty.


### -field DaylightDate

A 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains a date and local time when the transition from standard time to daylight saving time occurs on this operating system. If the time zone does not support daylight saving time or if the caller needs to disable daylight saving time, the <b>wMonth</b> member in the 
<b>SYSTEMTIME</b> structure must be zero. If this date is specified, the <b>StandardDate</b> member in this structure must also be specified. 


Otherwise, the system assumes the time zone data is invalid and no changes will be applied.

To select the correct day in the month, set the <b>wYear</b> member to zero, the <b>wHour</b> and <b>wMinute</b> members to the transition time, the <b>wDayOfWeek</b> member to the appropriate weekday, and the <b>wDay</b> member to indicate the occurrence of the day of the week within the month (1 to 5, where 5 indicates the final occurrence during the month if that day of the week does not occur 5 times).

If the <b>wYear</b> member is not zero, the transition date is absolute; it will only occur one time. Otherwise, it is a relative date that occurs yearly.


### -field DaylightBias

The bias value to be used during local time translations that occur during daylight saving time. This member is ignored if a value for the <b>DaylightDate</b> member is not supplied. 




This value is added to the value of the <b>Bias</b> member to form the bias used during daylight saving time. In most time zones, the value of this member is –60.


## -remarks



Settings for each time zone are stored in the following registry key:


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Time Zones</b>
                  <i>time_zone_name</i></pre>


Each time zone entry includes the following registry values.

<table>
<tr>
<th>Registry value</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td><b>Display</b></td>
<td>REG_SZ</td>
<td>The display name.</td>
</tr>
<tr>
<td><b>Dlt</b></td>
<td>REG_SZ</td>
<td>The description for daylight time.</td>
</tr>
<tr>
<td><b>MUI_Display</b></td>
<td>REG_SZ</td>
<td>The display name as a string of the form @<i>path</i>,<i>-stringID</i>[;<i>comment</i>]. For more information, see <a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">MUI</a>.</td>
</tr>
<tr>
<td><b>MUI_Dlt</b></td>
<td>REG_SZ</td>
<td>The description for daylight time as a string of the form @<i>path</i>,<i>-stringID</i>[;<i>comment</i>].</td>
</tr>
<tr>
<td><b>MUI_Std</b></td>
<td>REG_SZ</td>
<td>The description for standard time as a string of the form @<i>path</i>,<i>-stringID</i>[;<i>comment</i>].</td>
</tr>
<tr>
<td><b>Std</b></td>
<td>REG_SZ</td>
<td>The description for standard time.</td>
</tr>
<tr>
<td><b>TZI</b></td>
<td>REG_BINARY</td>
<td>
The following time zone information.

<pre class="syntax" xml:space="preserve"><code>typedef struct _REG_TZI_FORMAT
{
    LONG Bias;
    LONG StandardBias;
    LONG DaylightBias;
    SYSTEMTIME StandardDate;
    SYSTEMTIME DaylightDate;
} REG_TZI_FORMAT;
</code></pre>
</td>
</tr>
</table>
 

For more information about the <b>Dynamic DST</b> key, see <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>.

 Both <b>StandardName</b> and <b>DaylightName</b> are localized according to the current user default UI language.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/afb13501-3a87-433a-a05e-139103060109">SetTimeZoneInformation</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/3d7601a5-6d22-4b1a-a222-9db46d21a3c7">GetTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/afb13501-3a87-433a-a05e-139103060109">SetTimeZoneInformation</a>
 

 

