---
UID: NF:timezoneapi.FileTimeToSystemTime
title: FileTimeToSystemTime function (timezoneapi.h)
description: Converts a file time to system time format. System time is based on Coordinated Universal Time (UTC).
helpviewer_keywords: ["FileTimeToSystemTime","FileTimeToSystemTime function","_win32_filetimetosystemtime","base.filetimetosystemtime","timezoneapi/FileTimeToSystemTime","winbase/FileTimeToSystemTime"]
old-location: base\filetimetosystemtime.htm
tech.root: winprog
ms.assetid: d1d55f1f-4daa-4b9d-9962-873e38b1e0cf
ms.date: 12/05/2018
ms.keywords: FileTimeToSystemTime, FileTimeToSystemTime function, _win32_filetimetosystemtime, base.filetimetosystemtime, timezoneapi/FileTimeToSystemTime, winbase/FileTimeToSystemTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FileTimeToSystemTime
 - timezoneapi/FileTimeToSystemTime
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FileTimeToSystemTime
---

# FileTimeToSystemTime function


## -description

Converts a file time to system time format. System time is based on Coordinated Universal Time (UTC).

## -parameters

### -param lpFileTime [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the file 
       time to be converted to system (UTC) date and time format.

This value must be less than 0x8000000000000000. Otherwise, the function fails.

### -param lpSystemTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure to receive the 
      converted file time.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-dosdatetimetofiletime">DosDateTimeToFileTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/winbase/nf-winbase-filetimetodosdatetime">FileTimeToDosDateTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>