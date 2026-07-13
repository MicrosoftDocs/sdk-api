---
UID: NF:fileapi.FileTimeToLocalFileTime
title: FileTimeToLocalFileTime function (fileapi.h)
description: Converts a file time to a local file time.
helpviewer_keywords: ["FileTimeToLocalFileTime","FileTimeToLocalFileTime function","_win32_filetimetolocalfiletime","base.filetimetolocalfiletime","fileapi/FileTimeToLocalFileTime","winbase/FileTimeToLocalFileTime"]
old-location: base\filetimetolocalfiletime.htm
tech.root: winprog
ms.assetid: 58dfce16-2d7f-4db5-9f84-5dd651d26745
ms.date: 12/05/2018
ms.keywords: FileTimeToLocalFileTime, FileTimeToLocalFileTime function, _win32_filetimetolocalfiletime, base.filetimetolocalfiletime, fileapi/FileTimeToLocalFileTime, winbase/FileTimeToLocalFileTime
req.header: fileapi.h
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
 - FileTimeToLocalFileTime
 - fileapi/FileTimeToLocalFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FileTimeToLocalFileTime
---

# FileTimeToLocalFileTime function


## -description

Converts a file time to a local file time.

## -parameters

### -param lpFileTime [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the UTC-based file time to be converted into a local file time.

### -param lpLocalFileTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the converted local file time. This parameter cannot be the same as the <i>lpFileTime</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To account for daylight saving time when converting a file time to a local time, use the following sequence of functions in place of using <b>FileTimeToLocalFileTime</b>:
    
                

<ol>
<li>
<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>
</li>
<li>
<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime">SystemTimeToTzSpecificLocalTime</a>
</li>
<li>
<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>
</li>
</ol>

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-localfiletimetofiletime">LocalFileTimeToFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>