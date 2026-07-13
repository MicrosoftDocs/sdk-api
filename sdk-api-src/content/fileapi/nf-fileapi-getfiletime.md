---
UID: NF:fileapi.GetFileTime
title: GetFileTime function (fileapi.h)
description: Retrieves the date and time that a file or directory was created, last accessed, and last modified.
helpviewer_keywords: ["GetFileTime","GetFileTime function","_win32_getfiletime","base.getfiletime","fileapi/GetFileTime","winbase/GetFileTime"]
old-location: base\getfiletime.htm
tech.root: winprog
ms.assetid: 7f88e1c8-4328-40c2-857d-745e4a1d350d
ms.date: 12/05/2018
ms.keywords: GetFileTime, GetFileTime function, _win32_getfiletime, base.getfiletime, fileapi/GetFileTime, winbase/GetFileTime
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
 - GetFileTime
 - fileapi/GetFileTime
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
 - GetFileTime
---

# GetFileTime function


## -description

Retrieves the date and time that a file or directory was created, last accessed, and last 
    modified.

## -parameters

### -param hFile [in]

A handle to the file or directory for which dates and times are to be retrieved. The handle must have been 
      created using the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with the 
      <b>GENERIC_READ</b> access right. For more information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param lpCreationTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to receive the 
      date and time the file or directory was created. This parameter can be <b>NULL</b> if the 
      application does not require this information.

### -param lpLastAccessTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to 
      receive the date and time the file or directory was last accessed. The last access time includes the last time 
      the file or directory was written to, read from, or, in the case of executable files, run. This parameter can be 
      <b>NULL</b> if the application does not require this information.

### -param lpLastWriteTime [out, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to 
      receive the date and time the file or directory was last written to, truncated, or overwritten (for example, 
      with <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> or 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a>). This date and time is not updated when 
      file attributes or security descriptors are changed. This parameter can be <b>NULL</b> if the 
      application does not require this information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Not all file systems can record creation and last access times and not all file systems record them in the 
    same manner. For example, on  FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 
    2 seconds, and access time has a resolution of 1 day (really, the access date). Therefore, the 
    <b>GetFileTime</b> function may not return the same file time 
    information set using the <a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> function.

NTFS delays updates to the last access time for a file by up to one hour after the last access. NTFS also 
    permits last access time updates to be disabled. Last access time is not updated on NTFS volumes by default.

<b>Windows Server 2003 and Windows XP:  </b>Last access time is updated on NTFS volumes by default.

For more information, see <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

If you rename or delete a file, then restore it shortly thereafter, Windows searches the cache for file 
    information to restore. Cached information includes its short/long name pair and creation time.


#### Examples

For an example, see 
     <a href="/windows/desktop/SysInfo/retrieving-the-last-write-time">Retrieving the Last-Write Time</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletype">GetFileType</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>