---
UID: NF:winbase.FileTimeToDosDateTime
title: FileTimeToDosDateTime function (winbase.h)
description: Converts a file time to MS-DOS date and time values.
helpviewer_keywords: ["FileTimeToDosDateTime","FileTimeToDosDateTime function","_win32_filetimetodosdatetime","base.filetimetodosdatetime","winbase/FileTimeToDosDateTime"]
old-location: base\filetimetodosdatetime.htm
tech.root: winprog
ms.assetid: 7295da08-02f0-4390-862f-cf4267b69230
ms.date: 12/05/2018
ms.keywords: FileTimeToDosDateTime, FileTimeToDosDateTime function, _win32_filetimetodosdatetime, base.filetimetodosdatetime, winbase/FileTimeToDosDateTime
f1_keywords:
- winbase/FileTimeToDosDateTime
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
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
- FileTimeToDosDateTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FileTimeToDosDateTime function


## -description


Converts a file time to MS-DOS date and time values.


## -parameters




### -param lpFileTime [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the file time to convert to MS-DOS date and time format.


### -param lpFatDate [out]

A pointer to a variable to receive the MS-DOS date. The date is a packed value with the following format. 



<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0–4</td>
<td>Day of the month (1–31)</td>
</tr>
<tr>
<td>5–8</td>
<td>Month (1 = January, 2 = February, etc.)</td>
</tr>
<tr>
<td>9-15</td>
<td>Year offset from 1980 (add 1980 to get actual year)</td>
</tr>
</table>
 


### -param lpFatTime [out]

A pointer to a variable to receive the MS-DOS time. The time is a packed value with the following format. 



<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0–4</td>
<td>Second divided by 2</td>
</tr>
<tr>
<td>5–10</td>
<td>Minute (0–59)</td>
</tr>
<tr>
<td>11–15</td>
<td>Hour (0–23 on a 24-hour clock)</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The MS-DOS date format can represent only dates between 1/1/1980 and 12/31/2107; this conversion fails if the input file time is outside this range.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-dosdatetimetofiletime">DosDateTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>
 

 

