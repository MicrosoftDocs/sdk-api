---
UID: NS:minwinbase._SYSTEMTIME
title: SYSTEMTIME (minwinbase.h)
author: windows-sdk-content
description: Specifies a date and time, using individual members for the month, day, year, weekday, hour, minute, second, and millisecond. The time is either in coordinated universal time (UTC) or local time, depending on the function that is being called.
old-location: base\systemtime_str.htm
tech.root: SysInfo
ms.assetid: f77cdf86-0f97-4a89-b565-95b46fa7d65b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSYSTEMTIME, *PSYSTEMTIME, PSYSTEMTIME, PSYSTEMTIME structure pointer, SYSTEMTIME, SYSTEMTIME structure, _SYSTEMTIME, _win32_systemtime_str, base.systemtime_str, minwinbase/PSYSTEMTIME, minwinbase/SYSTEMTIME"
ms.topic: struct
f1_keywords: 
 - "minwinbase/SYSTEMTIME"
req.header: minwinbase.h
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
 - minwinbase.h
api_name:
 - SYSTEMTIME
product: Windows
targetos: Windows
req.typenames: SYSTEMTIME, *PSYSTEMTIME, *LPSYSTEMTIME
req.redist: 
ms.custom: 19H1
---

# SYSTEMTIME structure


## -description


Specifies a date and time, using individual members for the month, day, year, weekday, hour, minute, second, and millisecond. The time is either in coordinated universal time (UTC) or local time, depending on the function that is being called.


## -struct-fields




### -field wYear

 The year. The valid values for this member are 1601 through 30827.


### -field wMonth

The month. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
January

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
February

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
March

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
April

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
May

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
June

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
July

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
August

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9</dt>
</dl>
</td>
<td width="60%">
September

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
October

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
November

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>12</dt>
</dl>
</td>
<td width="60%">
December

</td>
</tr>
</table>
 


### -field wDayOfWeek

The day of the week. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
</table>
 


### -field wDay

The day of the month. The valid values for this member are 1 through 31.


### -field wHour

The hour. The valid values for this member are 0 through 23.


### -field wMinute

The minute. The valid values for this member are 0 through 59.


### -field wSecond

The second. The valid values for this member are 0 through 59.


### -field wMilliseconds

The millisecond. The valid values for this member are 0 through 999.


## -remarks



It is not recommended that you add and subtract values from the 
<b>SYSTEMTIME</b> structure to obtain relative times. Instead, you should

<ul>
<li>Convert the 
<b>SYSTEMTIME</b> structure to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.</li>
<li>Copy the resulting 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_ularge_integer">ULARGE_INTEGER</a> structure.</li>
<li>Use normal 64-bit arithmetic on the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_ularge_integer">ULARGE_INTEGER</a> value.</li>
</ul>
The system can periodically refresh the time by synchronizing with a time source. Because the system time can be adjusted either forward or backward, do not compare system time readings to determine elapsed time. Instead, use one of the methods described in 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/windows-time">Windows Time</a>.


#### Examples

The following example demonstrates the difference between the time values retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a> and <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a> functions.


```cpp
#include <windows.h>
#include <stdio.h>

void main()
{
    SYSTEMTIME st, lt;
    
    GetSystemTime(&st);
    GetLocalTime(&lt);
    
    printf("The system time is: %02d:%02d\n", st.wHour, st.wMinute);
    printf(" The local time is: %02d:%02d\n", lt.wHour, lt.wMinute);
}


```


<pre class="syntax" xml:space="preserve"><code>// Sample output

The system time is: 19:34
 The local time is: 12:34
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setlocaltime">SetLocalTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtime">SetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_ularge_integer">ULARGE_INTEGER</a>
 

 

