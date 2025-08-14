---
UID: NF:timezoneapi.SystemTimeToFileTime
title: SystemTimeToFileTime function (timezoneapi.h)
description: Converts a system time to file time format. System time is based on Coordinated Universal Time (UTC).
helpviewer_keywords: ["SystemTimeToFileTime","SystemTimeToFileTime function","_win32_systemtimetofiletime","base.systemtimetofiletime","timezoneapi/SystemTimeToFileTime"]
old-location: base\systemtimetofiletime.htm
tech.root: winprog
ms.assetid: d19594bc-8238-4a8f-882d-5b9019ef4880
ms.date: 12/05/2018
ms.keywords: SystemTimeToFileTime, SystemTimeToFileTime function, _win32_systemtimetofiletime, base.systemtimetofiletime, timezoneapi/SystemTimeToFileTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SystemTimeToFileTime
 - timezoneapi/SystemTimeToFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-timezone-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SystemTimeToFileTime
---

# SystemTimeToFileTime function


## -description

Converts a system time to file time format. System time is based on Coordinated Universal Time (UTC).

## -parameters

### -param lpSystemTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the system time to be converted from UTC to file time format. 




The <b>wDayOfWeek</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure is ignored.

### -param lpFileTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the converted system time.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

> [!NOTE]
> A False return value can indicate that the passed SYSTEMTIME structure represents an invalid date. Certain situations, such as the additional day added in a leap year, can result in application logic unexpectedly creating an invalid date. For more information on avoiding these issues, see [leap year readiness](https://techcommunity.microsoft.com/t5/azure-developer-community-blog/it-s-2020-is-your-code-ready-for-leap-day/ba-p/1157279).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-dosdatetimetofiletime">DosDateTimeToFileTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winbase/nf-winbase-filetimetodosdatetime">FileTimeToDosDateTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>