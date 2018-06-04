---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetFileTime function


## -description


Sets the date and time that the specified file or directory was created, last accessed, or last 
    modified.


## -parameters




### -param hFile [in]

A handle to the file or directory. The handle must have been created using the 
      <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function  with the 
      <b>FILE_WRITE_ATTRIBUTES</b> access right. For more information, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param lpCreationTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the 
      new creation date and time for the file or directory. If 
      the application does not need to change this information, set this parameter either to <b>NULL</b> or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.


### -param lpLastAccessTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that 
       contains the new last access date and time for the file or directory. The last access time includes the last 
       time the file or directory was written to, read from, or (in the case of executable files) run. If 
      the application does not need to change this information, set this parameter 
       either to <b>NULL</b> or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.

To prevent file operations using the given handle from modifying the last access time, call 
       <b>SetFileTime</b> immediately  after opening the file handle 
       and pass a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that has both the 
       <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 
       0xFFFFFFFF.


### -param lpLastWriteTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that 
       contains the new last modified date and time for the file or directory.  If the application does not need to change this information, set this parameter either  to <b>NULL</b>  or to a pointer to a <b>FILETIME</b> structure that has both the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 0.

To prevent file operations using the given handle from modifying the last access time, call 
       <b>SetFileTime</b> immediately after opening the file handle 
       and pass a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that has both the 
       <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members set to 
       0xFFFFFFFF.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Not all file systems can record creation and last access times and not all file systems record them in the 
    same manner. For example, on  FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 
    2 seconds, and access time has a resolution of 1 day (really, the access date). Therefore, the 
    <a href="https://msdn.microsoft.com/7f88e1c8-4328-40c2-857d-745e4a1d350d">GetFileTime</a> function may not return the same file time 
    information set using <b>SetFileTime</b>. NTFS delays updates to 
    the last access time for a file by up to one hour after the last access.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/b4a70c01-d5ce-47e8-9918-9c9176894240">Changing a File Time to the Current Time</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>



<a href="https://msdn.microsoft.com/7f88e1c8-4328-40c2-857d-745e4a1d350d">GetFileTime</a>



<a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

