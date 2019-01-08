---
UID: NF:timezoneapi.FileTimeToSystemTime
title: FileTimeToSystemTime function
author: windows-sdk-content
description: Converts a file time to system time format. System time is based on Coordinated Universal Time (UTC).
old-location: base\filetimetosystemtime.htm
tech.root: SysInfo
ms.assetid: d1d55f1f-4daa-4b9d-9962-873e38b1e0cf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FileTimeToSystemTime, FileTimeToSystemTime function, _win32_filetimetosystemtime, base.filetimetosystemtime, timezoneapi/FileTimeToSystemTime, winbase/FileTimeToSystemTime
ms.topic: function
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FileTimeToSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FileTimeToSystemTime function


## -description


Converts a file time to system time format. System time is based on Coordinated Universal Time (UTC).


## -parameters




### -param lpFileTime [in]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the file 
       time to be converted to system (UTC) date and time format.

This value must be less than 0x8000000000000000. Otherwise, the function fails.


### -param lpSystemTime [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure to receive the 
      converted file time.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/33459ef5-e310-4fe0-bdda-e1db2ffd4888">DosDateTimeToFileTime</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/7295da08-02f0-4390-862f-cf4267b69230">FileTimeToDosDateTime</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

