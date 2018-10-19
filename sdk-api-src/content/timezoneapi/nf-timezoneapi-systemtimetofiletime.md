---
UID: NF:timezoneapi.SystemTimeToFileTime
title: SystemTimeToFileTime function
author: windows-sdk-content
description: Converts a system time to file time format. System time is based on Coordinated Universal Time (UTC).
old-location: base\systemtimetofiletime.htm
tech.root: sysinfo
ms.assetid: d19594bc-8238-4a8f-882d-5b9019ef4880
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: SystemTimeToFileTime, SystemTimeToFileTime function, _win32_systemtimetofiletime, base.systemtimetofiletime, timezoneapi/SystemTimeToFileTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SystemTimeToFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SystemTimeToFileTime function


## -description


Converts a system time to file time format. System time is based on Coordinated Universal Time (UTC).


## -parameters




### -param lpSystemTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the system time to be converted from UTC to file time format. 




The <b>wDayOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure is ignored.


### -param lpFileTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to receive the converted system time.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/33459ef5-e310-4fe0-bdda-e1db2ffd4888">DosDateTimeToFileTime</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/7295da08-02f0-4390-862f-cf4267b69230">FileTimeToDosDateTime</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

