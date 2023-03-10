---
UID: NS:timezoneapi._TIME_DYNAMIC_ZONE_INFORMATION
title: DYNAMIC_TIME_ZONE_INFORMATION (timezoneapi.h)
description: Specifies settings for a time zone and dynamic daylight saving time.
helpviewer_keywords: ["*PDYNAMIC_TIME_ZONE_INFORMATION","DYNAMIC_TIME_ZONE_INFORMATION","DYNAMIC_TIME_ZONE_INFORMATION structure","PDYNAMIC_TIME_ZONE_INFORMATION","PDYNAMIC_TIME_ZONE_INFORMATION structure pointer","_TIME_DYNAMIC_ZONE_INFORMATION","_TIME_DYNAMIC_ZONE_INFORMATION structure","base.dynamic_time_zone_information","winbase/PDYNAMIC_TIME_ZONE_INFORMATION","winbase/_DYNAMIC_TIME_ZONE_INFORMATION"]
old-location: base\dynamic_time_zone_information.htm
tech.root: winprog
ms.assetid: d60b1212-26bc-4fad-afce-9bd9062ca5b0
ms.date: 12/05/2018
ms.keywords: '*PDYNAMIC_TIME_ZONE_INFORMATION, DYNAMIC_TIME_ZONE_INFORMATION, DYNAMIC_TIME_ZONE_INFORMATION structure, PDYNAMIC_TIME_ZONE_INFORMATION, PDYNAMIC_TIME_ZONE_INFORMATION structure pointer, _TIME_DYNAMIC_ZONE_INFORMATION, _TIME_DYNAMIC_ZONE_INFORMATION structure, base.dynamic_time_zone_information, winbase/PDYNAMIC_TIME_ZONE_INFORMATION, winbase/_DYNAMIC_TIME_ZONE_INFORMATION'
req.header: timezoneapi.h
req.include-header: Timezoneapi.h, Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DYNAMIC_TIME_ZONE_INFORMATION, *PDYNAMIC_TIME_ZONE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TIME_DYNAMIC_ZONE_INFORMATION
 - timezoneapi/_TIME_DYNAMIC_ZONE_INFORMATION
 - PDYNAMIC_TIME_ZONE_INFORMATION
 - timezoneapi/PDYNAMIC_TIME_ZONE_INFORMATION
 - DYNAMIC_TIME_ZONE_INFORMATION
 - timezoneapi/DYNAMIC_TIME_ZONE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - DYNAMIC_TIME_ZONE_INFORMATION
---

# DYNAMIC_TIME_ZONE_INFORMATION structure


## -description

Specifies settings for  a time zone and dynamic daylight saving time.

## -struct-fields

### -field Bias

The current bias for local time translation on this computer, in minutes. The bias is the difference, in 
       minutes, between Coordinated Universal Time (UTC) and local time. All translations between UTC and local time 
       are based on the following formula:

UTC = local time + bias

This member is required.

### -field StandardName

A description for standard time. For example, "EST" could indicate Eastern Standard Time. The string will 
      be returned unchanged by the 
      <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a> 
      function. This string can be empty.

### -field StandardDate

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains a date and 
       local time when the transition from daylight saving time to standard time occurs on this operating system. If 
       the time zone does not support daylight saving time or if the caller needs to disable daylight saving time, the 
       <b>wMonth</b> member in the 
       <b>SYSTEMTIME</b> structure must be zero. If this date is 
       specified, the <b>DaylightDate</b> member of this structure must also be specified. 
       Otherwise, the system assumes the time zone data is invalid and no changes will be applied.

To select the correct day in the month, set the <b>wYear</b> member to zero, the 
       <b>wHour</b> and <b>wMinute</b> members to the transition time, the 
       <b>wDayOfWeek</b> member to the appropriate weekday, and the 
       <b>wDay</b> member to indicate the occurrence of the day of the week within the month (1 to 
       5, where 5 indicates the final occurrence during the month if that day of the week does not occur 5 times).

Using this notation, specify 02:00 on the first Sunday in April as follows: 
       <b>wHour</b> = 2, <b>wMonth</b> = 4, 
       <b>wDayOfWeek</b> = 0, <b>wDay</b> = 1. Specify 02:00 on the last 
       Thursday in October as follows: <b>wHour</b> = 2, <b>wMonth</b> = 10, 
       <b>wDayOfWeek</b> = 4, <b>wDay</b> = 5.

If the 
       <b>wYear</b> member is not zero, the transition date is absolute; it will only occur one 
       time. Otherwise, it is a relative date that occurs yearly.

### -field StandardBias

The bias value to be used during local time translations that occur during standard time. This member is 
       ignored if a value for the <b>StandardDate</b> member is not supplied.

This value is added to the value of the <b>Bias</b> member to form the bias used during 
       standard time. In most time zones, the value of this member is zero.

### -field DaylightName

A description for daylight saving time (DST). For example, "PDT" could indicate Pacific Daylight Time. The 
      string will be  returned unchanged by the 
      <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a> 
      function. This string can be empty.

### -field DaylightDate

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains a 
       date and local time when the transition from standard time to daylight saving time occurs on this operating 
       system. If the time zone does not support daylight saving time or if the caller needs to disable daylight 
       saving time, the <b>wMonth</b> member in the 
       <b>SYSTEMTIME</b> structure must be zero. If this date is 
       specified, the <b>StandardDate</b> member in this structure must also be specified. 
       Otherwise, the system assumes the time zone data is invalid and no changes will be applied.

To select the correct day in the month, set the <b>wYear</b> member to zero, the 
       <b>wHour</b> and <b>wMinute</b> members to the transition time, the 
       <b>wDayOfWeek</b> member to the appropriate weekday, and the 
       <b>wDay</b> member to indicate the occurrence of the day of the week within the month (1 to 
       5, where 5 indicates the final occurrence during the month if that day of the week does not occur 5 times).

If the <b>wYear</b> member is not zero, the transition date is absolute; it will only 
       occur one time. Otherwise, it is a relative date that occurs yearly.

### -field DaylightBias

The bias value to be used during local time translations that occur during daylight saving time. This member 
       is ignored if a value for the <b>DaylightDate</b> member is not supplied.

This value is added to the value of the <b>Bias</b> member to form the bias used during 
       daylight saving time. In most time zones, the value of this member is –60.

### -field TimeZoneKeyName

The name of the time zone registry key on the local computer. For more information, see Remarks.

### -field DynamicDaylightTimeDisabled

Indicates whether dynamic daylight saving time is disabled. Setting this member to <b>TRUE</b> disables dynamic 
       daylight saving time, causing the system to use a fixed set of transition dates.

To restore dynamic daylight saving time, call the 
       <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a> 
       function with <b>DynamicDaylightTimeDisabled</b> set to <b>FALSE</b>. 
       The system will read the transition dates for the current year at the next time update, the next system reboot, 
       or the end of the calendar year (whichever comes first.)

When calling the 
       <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a> 
       function, this member is <b>TRUE</b> if the time zone was set using the 
       <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-settimezoneinformation">SetTimeZoneInformation</a> function instead of 
       <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a> or if 
       the user has disabled this feature using the Date and Time application in Control 
       Panel.

To disable daylight saving time, set this member to <b>TRUE</b>, clear the 
       <b>StandardDate</b> and <b>DaylightDate</b> members, and call 
       <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a>. To 
       restore daylight saving time, call 
       <b>SetDynamicTimeZoneInformation</b> with 
       <b>DynamicDaylightTimeDisabled</b> set to <b>FALSE</b>.

## -remarks

Dynamic daylight saving time provides support for time zones whose boundaries for daylight saving time change 
    from year to year. This feature enables easier updating of systems, especially for locales where the yearly DST 
    boundaries are known in advance. After the time zone has been updated, the current time zone setting is applied to 
    all time operations, even when the time in question occurred before the time zone changed. Therefore, it is best 
    to store UTC times and convert them to the current local time zone.

You can set the transition dates for the current year using the 
     <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a> function. 
     To set future transition dates, you must add entries to the registry data. The settings for dynamic daylight time 
     are stored in the following registry key:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Time Zones</b>
                  <i>time_zone_name</i>
                     <b>Dynamic DST</b></pre>


Each <b>Dynamic DST</b> key includes the following registry values.

<table>
<tr>
<th>Registry value</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td><b>FirstEntry</b></td>
<td><b>REG_DWORD</b></td>
<td>The first year in the table.</td>
</tr>
<tr>
<td><b>LastEntry</b></td>
<td><b>REG_DWORD</b></td>
<td>The last year in the table.</td>
</tr>
<tr>
<td><i>year1</i></td>
<td><b>REG_BINARY</b></td>
<td>
The following time zone information.


``` syntax
typedef struct _REG_TZI_FORMAT
{
    LONG Bias;
    LONG StandardBias;
    LONG DaylightBias;
    SYSTEMTIME StandardDate;
    SYSTEMTIME DaylightDate;
} REG_TZI_FORMAT;
```

</td>
</tr>
<tr>
<td><i>year2</i></td>
<td><b>REG_BINARY</b></td>
<td>A <b>REG_TZI_FORMAT</b> structure.</td>
</tr>
<tr>
<td><i>yearN</i></td>
<td><b>REG_BINARY</b></td>
<td>A <b>REG_TZI_FORMAT</b> structure.</td>
</tr>
</table>
 

For more information on other values in the <b>Time Zones</b> key, see 
     <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>.

 Both <b>StandardName</b> and <b>DaylightName</b> are localized according to the current user default UI language.

## -see-also

<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a>
