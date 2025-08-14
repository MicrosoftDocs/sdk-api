---
UID: NF:fileapi.LocalFileTimeToFileTime
title: LocalFileTimeToFileTime function (fileapi.h)
description: Converts a local file time to a file time based on the Coordinated Universal Time (UTC).
helpviewer_keywords: ["LocalFileTimeToFileTime","LocalFileTimeToFileTime function","_win32_localfiletimetofiletime","base.localfiletimetofiletime","fileapi/LocalFileTimeToFileTime","winbase/LocalFileTimeToFileTime"]
old-location: base\localfiletimetofiletime.htm
tech.root: winprog
ms.assetid: 491e4724-8e6f-4155-b427-15cd7968e2da
ms.date: 12/05/2018
ms.keywords: LocalFileTimeToFileTime, LocalFileTimeToFileTime function, _win32_localfiletimetofiletime, base.localfiletimetofiletime, fileapi/LocalFileTimeToFileTime, winbase/LocalFileTimeToFileTime
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
 - LocalFileTimeToFileTime
 - fileapi/LocalFileTimeToFileTime
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
 - LocalFileTimeToFileTime
---

# LocalFileTimeToFileTime function


## -description

Converts a local file time to a file time based on the Coordinated Universal Time (UTC).

## -parameters

### -param lpLocalFileTime [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the 
      local file time to be converted into a UTC-based file time.

### -param lpFileTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the 
      converted UTC-based file time. This parameter cannot be the same as the 
      <i>lpLocalFileTime</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

<b>LocalFileTimeToFileTime</b> uses the current 
    settings for the time zone and daylight saving time. Therefore, if it is daylight saving time, this function will 
    take daylight saving time into account, even if the time you are converting is in standard time.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime">FileTimeToLocalFileTime</a>



<a href="/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>