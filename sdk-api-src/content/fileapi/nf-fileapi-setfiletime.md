---
UID: NF:fileapi.SetFileTime
title: SetFileTime function (fileapi.h)
description: Sets the date and time that the specified file or directory was created, last accessed, or last modified.
helpviewer_keywords: ["SetFileTime","SetFileTime function","_win32_setfiletime","base.setfiletime","fileapi/SetFileTime","winbase/SetFileTime"]
old-location: base\setfiletime.htm
tech.root: winprog
ms.assetid: 75d988e4-22a3-4084-a5f8-1fca73ccd542
ms.date: 12/05/2018
ms.keywords: SetFileTime, SetFileTime function, _win32_setfiletime, base.setfiletime, fileapi/SetFileTime, winbase/SetFileTime
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
 - SetFileTime
 - fileapi/SetFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetFileTime
---

# SetFileTime function


## -description

Sets the date and time that the specified file or directory was created, last accessed, or last 
    modified.

## -parameters

### -param hFile [in]

A handle to the file or directory. The handle must have been created using the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function  with the 
      <b>FILE_WRITE_ATTRIBUTES</b> access right. For more information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param lpCreationTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the 
      new creation date and time for the file or directory. If 
      the application does not need to change this information, set this parameter either to <b>NULL</b> or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.

### -param lpLastAccessTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that 
       contains the new last access date and time for the file or directory. The last access time includes the last 
       time the file or directory was written to, read from, or (in the case of executable files) run. If 
      the application does not need to change this information, set this parameter 
       either to <b>NULL</b> or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.

To prevent file operations using the given handle from modifying the last access time, call 
       <b>SetFileTime</b> immediately  after opening the file handle 
       and pass a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that has both the 
       <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 
       0xFFFFFFFF.

### -param lpLastWriteTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that 
       contains the new last modified date and time for the file or directory.  If the application does not need to change this information, set this parameter either  to <b>NULL</b>  or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Not all file systems can record creation and last access times and not all file systems record them in the 
    same manner. For example, on  FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 
    2 seconds, and access time has a resolution of 1 day (really, the access date). Therefore, the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a> function may not return the same file time 
    information set using <b>SetFileTime</b>. NTFS delays updates to 
    the last access time for a file by up to one hour after the last access.


#### Examples

For an example, see 
     <a href="/windows/desktop/SysInfo/changing-a-file-time-to-the-current-time">Changing a File Time to the Current Time</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletype">GetFileType</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>
