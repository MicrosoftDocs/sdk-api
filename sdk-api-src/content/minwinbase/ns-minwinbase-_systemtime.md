---
UID: NS:minwinbase._SYSTEMTIME
title: "_SYSTEMTIME"
author: windows-sdk-content
description: Specifies a date and time, using individual members for the month, day, year, weekday, hour, minute, second, and millisecond. The time is either in coordinated universal time (UTC) or local time, depending on the function that is being called.
old-location: base\systemtime_str.htm
tech.root: sysinfo
ms.assetid: f77cdf86-0f97-4a89-b565-95b46fa7d65b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPSYSTEMTIME, *PSYSTEMTIME, PSYSTEMTIME, PSYSTEMTIME structure pointer, SYSTEMTIME, SYSTEMTIME structure, _SYSTEMTIME, _win32_systemtime_str, base.systemtime_str, minwinbase/PSYSTEMTIME, minwinbase/SYSTEMTIME"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
---

# _SYSTEMTIME structure


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
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.</li>
<li>Copy the resulting 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to a 
<a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure.</li>
<li>Use normal 64-bit arithmetic on the <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> value.</li>
</ul>
The system can periodically refresh the time by synchronizing with a time source. Because the system time can be adjusted either forward or backward, do not compare system time readings to determine elapsed time. Instead, use one of the methods described in 
<a href="https://msdn.microsoft.com/95c00204-bfdf-4376-9aae-8d8139ba6750">Windows Time</a>.


#### Examples

The following example demonstrates the difference between the time values retrieved by the <a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a> and <a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a> functions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;

void main()
{
    SYSTEMTIME st, lt;
    
    GetSystemTime(&amp;st);
    GetLocalTime(&amp;lt);
    
    printf("The system time is: %02d:%02d\n", st.wHour, st.wMinute);
    printf(" The local time is: %02d:%02d\n", lt.wHour, lt.wMinute);
}

</pre>
</td>
</tr>
</table></span></div>
<pre class="syntax" xml:space="preserve"><code>// Sample output

The system time is: 19:34
 The local time is: 12:34
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a>



<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/c2d2bac7-4171-4b8b-81e8-0e8a1b2794e6">SetLocalTime</a>



<a href="https://msdn.microsoft.com/0768794d-de61-4d5c-96ad-4c4711c72584">SetSystemTime</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>
 

 

