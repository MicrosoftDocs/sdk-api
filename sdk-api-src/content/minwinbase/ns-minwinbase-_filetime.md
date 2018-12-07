---
UID: NS:minwinbase._FILETIME
title: "_FILETIME"
author: windows-sdk-content
description: Contains a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).
old-location: base\filetime_str.htm
tech.root: sysinfo
ms.assetid: 9baf8a0e-59e3-4fbd-9616-2ec9161520d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPFILETIME, *PFILETIME, FILETIME, FILETIME structure, PFILETIME, PFILETIME structure pointer, _FILETIME, _win32_filetime_str, base.filetime_str, minwinbase/FILETIME, minwinbase/PFILETIME"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - FILETIME
product: Windows
targetos: Windows
req.typenames: FILETIME, *PFILETIME, *LPFILETIME
req.redist: 
---

# _FILETIME structure


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
<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a> function.

It is not recommended that you add and subtract values from the 
<b>FILETIME</b> structure to obtain relative times. Instead, you should copy the low- and high-order parts of the file time to a <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure, perform 64-bit arithmetic on the <b>QuadPart</b> member, and copy the <b>LowPart</b> and <b>HighPart</b> members into the <b>FILETIME</b> structure.

Do not cast a pointer to a <b>FILETIME</b> structure to either a <b>ULARGE_INTEGER*</b> or <b>__int64*</b> value because it can cause alignment faults on 64-bit Windows.

Not all file systems can record creation and last access time and not all file systems record them in the same manner. For example, on NT FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date). On NTFS, access time has a resolution of 1 hour. Therefore, the 
<a href="https://msdn.microsoft.com/7f88e1c8-4328-40c2-857d-745e4a1d350d">GetFileTime</a> function may not return the same file time information set using the 
<a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> function. Furthermore, FAT records times on disk in local time. However, NTFS records times on disk in UTC. For more information, see 
<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>.

  A function using the <b>FILETIME</b> structure can allow for values outside of  zero or positive values typically specified by the <b>dwLowDateTime</b> and <b>dwHighDateTime</b> members.  For example, the <a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> function uses 0xFFFFFFFF to specify that a file's previous access time should be preserved. For more information, see the topic for the function you are calling.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b4a70c01-d5ce-47e8-9918-9c9176894240">Changing a File Time to the Current Time</a> or <a href="https://msdn.microsoft.com/54509a35-fa6a-4ee6-90f8-36c9ef55e1bc">Retrieving the Last-Write Time</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/38161826-3a43-42a3-a49d-415b5f7451c5">CompareFileTime</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/7f88e1c8-4328-40c2-857d-745e4a1d350d">GetFileTime</a>



<a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>
 

 

