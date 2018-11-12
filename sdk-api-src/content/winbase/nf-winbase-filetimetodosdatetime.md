---
UID: NF:winbase.FileTimeToDosDateTime
title: FileTimeToDosDateTime function
author: windows-sdk-content
description: Converts a file time to MS-DOS date and time values.
old-location: base\filetimetodosdatetime.htm
tech.root: sysinfo
ms.assetid: 7295da08-02f0-4390-862f-cf4267b69230
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: FileTimeToDosDateTime, FileTimeToDosDateTime function, _win32_filetimetodosdatetime, base.filetimetodosdatetime, winbase/FileTimeToDosDateTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FileTimeToDosDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FileTimeToDosDateTime function


## -description


Converts a file time to MS-DOS date and time values.


## -parameters




### -param lpFileTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the file time to convert to MS-DOS date and time format.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The MS-DOS date format can represent only dates between 1/1/1980 and 12/31/2107; this conversion fails if the input file time is outside this range.




## -see-also




<a href="https://msdn.microsoft.com/33459ef5-e310-4fe0-bdda-e1db2ffd4888">DosDateTimeToFileTime</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

