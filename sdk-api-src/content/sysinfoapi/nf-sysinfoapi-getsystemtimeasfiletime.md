---
UID: NF:sysinfoapi.GetSystemTimeAsFileTime
title: GetSystemTimeAsFileTime function (sysinfoapi.h)
description: Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.
helpviewer_keywords: ["GetSystemTimeAsFileTime","GetSystemTimeAsFileTime function","_win32_getsystemtimeasfiletime","base.getsystemtimeasfiletime","sysinfoapi/GetSystemTimeAsFileTime"]
old-location: base\getsystemtimeasfiletime.htm
tech.root: winprog
ms.assetid: adf7ff5d-2d30-4490-9868-9ad78ef7a0b6
ms.date: 12/05/2018
ms.keywords: GetSystemTimeAsFileTime, GetSystemTimeAsFileTime function, _win32_getsystemtimeasfiletime, base.getsystemtimeasfiletime, sysinfoapi/GetSystemTimeAsFileTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemTimeAsFileTime
 - sysinfoapi/GetSystemTimeAsFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
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
---

# GetSystemTimeAsFileTime function


## -description

Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.

## -parameters

### -param lpSystemTimeAsFileTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the current system date and time in UTC format.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>