---
UID: NF:winbase.DosDateTimeToFileTime
title: DosDateTimeToFileTime function (winbase.h)
author: windows-sdk-content
description: Converts MS-DOS date and time values to a file time.
old-location: base\dosdatetimetofiletime.htm
tech.root: SysInfo
ms.assetid: 33459ef5-e310-4fe0-bdda-e1db2ffd4888
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DosDateTimeToFileTime, DosDateTimeToFileTime function, _win32_dosdatetimetofiletime, base.dosdatetimetofiletime, winbase/DosDateTimeToFileTime
ms.topic: function
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
 - DosDateTimeToFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the converted file time.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/7295da08-02f0-4390-862f-cf4267b69230">FileTimeToDosDateTime</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

