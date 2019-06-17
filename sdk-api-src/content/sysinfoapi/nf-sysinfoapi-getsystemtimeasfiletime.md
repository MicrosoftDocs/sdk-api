---
UID: NF:sysinfoapi.GetSystemTimeAsFileTime
title: GetSystemTimeAsFileTime function (sysinfoapi.h)
author: windows-sdk-content
description: Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.
old-location: base\getsystemtimeasfiletime.htm
tech.root: SysInfo
ms.assetid: adf7ff5d-2d30-4490-9868-9ad78ef7a0b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemTimeAsFileTime, GetSystemTimeAsFileTime function, _win32_getsystemtimeasfiletime, base.getsystemtimeasfiletime, sysinfoapi/GetSystemTimeAsFileTime
ms.topic: function
f1_keywords: ["sysinfoapi/GetSystemTimeAsFileTime"]
req.header: sysinfoapi.h
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
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemTimeAsFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemTimeAsFileTime function


## -description


Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.


## -parameters




### -param lpSystemTimeAsFileTime [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the current system date and time in UTC format.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/file-times">File Times</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-time">System Time</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>
 

 

