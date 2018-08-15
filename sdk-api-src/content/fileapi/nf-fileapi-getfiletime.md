---
UID: NF:fileapi.GetFileTime
title: GetFileTime function
author: windows-sdk-content
description: Retrieves the date and time that a file or directory was created, last accessed, and last modified.
old-location: base\getfiletime.htm
old-project: SysInfo
ms.assetid: 7f88e1c8-4328-40c2-857d-745e4a1d350d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetFileTime, GetFileTime function, _win32_getfiletime, base.getfiletime, fileapi/GetFileTime, winbase/GetFileTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: STREAM_INFO_LEVELS
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
 - GetFileTime
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetFileTime function


## -description


Retrieves the date and time that a file or directory was created, last accessed, and last 
    modified.


## -parameters




### -param hFile [in]

A handle to the file or directory for which dates and times are to be retrieved. The handle must have been 
      created using the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with the 
      <b>GENERIC_READ</b> access right. For more information, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param lpCreationTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to receive the 
      date and time the file or directory was created. This parameter can be <b>NULL</b> if the 
      application does not require this information.


### -param lpLastAccessTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to 
      receive the date and time the file or directory was last accessed. The last access time includes the last time 
      the file or directory was written to, read from, or, in the case of executable files, run. This parameter can be 
      <b>NULL</b> if the application does not require this information.


### -param lpLastWriteTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to 
      receive the date and time the file or directory was last written to, truncated, or overwritten (for example, 
      with <a href="base.writefile">WriteFile</a> or 
      <a href="base.setendoffile">SetEndOfFile</a>). This date and time is not updated when 
      file attributes or security descriptors are changed. This parameter can be <b>NULL</b> if the 
      application does not require this information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Not all file systems can record creation and last access times and not all file systems record them in the 
    same manner. For example, on  FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 
    2 seconds, and access time has a resolution of 1 day (really, the access date). Therefore, the 
    <b>GetFileTime</b> function may not return the same file time 
    information set using the <a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> function.

NTFS delays updates to the last access time for a file by up to one hour after the last access. NTFS also 
    permits last access time updates to be disabled. Last access time is not updated on NTFS volumes by default.

<b>Windows Server 2003 and Windows XP:  </b>Last access time is updated on NTFS volumes by default.

For more information, see <a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>.

If you rename or delete a file, then restore it shortly thereafter, Windows searches the cache for file 
    information to restore. Cached information includes its short/long name pair and creation time.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/54509a35-fa6a-4ee6-90f8-36c9ef55e1bc">Retrieving the Last-Write Time</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>



<a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a>



<a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

