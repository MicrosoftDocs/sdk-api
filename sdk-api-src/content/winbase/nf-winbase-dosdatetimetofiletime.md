---
UID: NF:winbase.DosDateTimeToFileTime
title: DosDateTimeToFileTime function (winbase.h)
description: Converts MS-DOS date and time values to a file time.
helpviewer_keywords: ["DosDateTimeToFileTime","DosDateTimeToFileTime function","_win32_dosdatetimetofiletime","base.dosdatetimetofiletime","winbase/DosDateTimeToFileTime"]
old-location: base\dosdatetimetofiletime.htm
tech.root: winprog
ms.assetid: 33459ef5-e310-4fe0-bdda-e1db2ffd4888
ms.date: 12/05/2018
ms.keywords: DosDateTimeToFileTime, DosDateTimeToFileTime function, _win32_dosdatetimetofiletime, base.dosdatetimetofiletime, winbase/DosDateTimeToFileTime
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DosDateTimeToFileTime
 - winbase/DosDateTimeToFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - DosDateTimeToFileTime
---

# DosDateTimeToFileTime function


## -description

Converts MS-DOS date and time values to a file time.

## -parameters

### -param wFatDate [in]

The MS-DOS date. The date is a packed value with the following format. 



<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Day of the month (1–31)</td>
</tr>
<tr>
<td>5-8</td>
<td>Month (1 = January, 2 = February, and so on)</td>
</tr>
<tr>
<td>9-15</td>
<td>Year offset from 1980 (add 1980 to get actual year)</td>
</tr>
</table>

### -param wFatTime [in]

The MS-DOS time. The time is a packed value with the following format. 



<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Second divided by 2</td>
</tr>
<tr>
<td>5-10</td>
<td>Minute (0–59)</td>
</tr>
<tr>
<td>11-15</td>
<td>Hour (0–23 on a 24-hour clock)</td>
</tr>
</table>

### -param lpFileTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the converted file time.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winbase/nf-winbase-filetimetodosdatetime">FileTimeToDosDateTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>