---
UID: NS:minwinbase._FILETIME
title: FILETIME (minwinbase.h)
description: Contains a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).
helpviewer_keywords: ["*LPFILETIME","*PFILETIME","FILETIME","FILETIME structure","PFILETIME","PFILETIME structure pointer","_FILETIME","_win32_filetime_str","base.filetime_str","minwinbase/FILETIME","minwinbase/PFILETIME"]
old-location: base\filetime_str.htm
tech.root: winprog
ms.assetid: 9baf8a0e-59e3-4fbd-9616-2ec9161520d1
ms.date: 12/05/2018
ms.keywords: '*LPFILETIME, *PFILETIME, FILETIME, FILETIME structure, PFILETIME, PFILETIME structure pointer, _FILETIME, _win32_filetime_str, base.filetime_str, minwinbase/FILETIME, minwinbase/PFILETIME'
req.header: minwinbase.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILETIME, *PFILETIME, *LPFILETIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILETIME
 - minwinbase/_FILETIME
 - PFILETIME
 - minwinbase/PFILETIME
 - FILETIME
 - minwinbase/FILETIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - FILETIME
---

# FILETIME structure


## -description

Contains a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).

## -struct-fields

### -field dwLowDateTime

The low-order part of the file time.

### -field dwHighDateTime

The high-order part of the file time.

## -remarks

To convert a 
<b>FILETIME</b> structure into a time that is easy to display to a user, use the 
<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a> function.

It is not recommended that you add and subtract values from the 
<b>FILETIME</b> structure to obtain relative times. Instead, you should copy the low- and high-order parts of the file time to a <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a> structure, perform 64-bit arithmetic on the <b>QuadPart</b> member, and copy the <b>LowPart</b> and <b>HighPart</b> members into the <b>FILETIME</b> structure.

Do not cast a pointer to a <b>FILETIME</b> structure to either a <b>ULARGE_INTEGER*</b> or <b>__int64*</b> value because it can cause alignment faults on 64-bit Windows.

Not all file systems can record creation and last access time and not all file systems record them in the same manner. For example, on NT FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date). On NTFS, access time has a resolution of 1 hour. Therefore, the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a> function may not return the same file time information set using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> function. Furthermore, FAT records times on disk in local time. However, NTFS records times on disk in UTC. For more information, see 
<a href="/windows/desktop/SysInfo/file-times">File Times</a>.

  A function using the <b>FILETIME</b> structure can allow for values outside of  zero or positive values typically specified by the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members.  For example, the <a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> function uses 0xFFFFFFFF to specify that a file's previous access time should be preserved. For more information, see the topic for the function you are calling.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/changing-a-file-time-to-the-current-time">Changing a File Time to the Current Time</a> or <a href="/windows/desktop/SysInfo/retrieving-the-last-write-time">Retrieving the Last-Write Time</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-comparefiletime">CompareFileTime</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a>



<a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a>