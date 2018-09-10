---
UID: NF:fileapi.LocalFileTimeToFileTime
title: LocalFileTimeToFileTime function
author: windows-sdk-content
description: Converts a local file time to a file time based on the Coordinated Universal Time (UTC).
old-location: base\localfiletimetofiletime.htm
tech.root: SysInfo
ms.assetid: 491e4724-8e6f-4155-b427-15cd7968e2da
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LocalFileTimeToFileTime, LocalFileTimeToFileTime function, _win32_localfiletimetofiletime, base.localfiletimetofiletime, fileapi/LocalFileTimeToFileTime, winbase/LocalFileTimeToFileTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - LocalFileTimeToFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LocalFileTimeToFileTime function


## -description


Converts a local file time to a file time based on the Coordinated Universal Time (UTC).


## -parameters




### -param lpLocalFileTime [in]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies the 
      local file time to be converted into a UTC-based file time.


### -param lpFileTime [out]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to receive the 
      converted UTC-based file time. This parameter cannot be the same as the 
      <i>lpLocalFileTime</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



<b>LocalFileTimeToFileTime</b> uses the current 
    settings for the time zone and daylight saving time. Therefore, if it is daylight saving time, this function will 
    take daylight saving time into account, even if the time you are converting is in standard time.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/58dfce16-2d7f-4db5-9f84-5dd651d26745">FileTimeToLocalFileTime</a>



<a href="https://msdn.microsoft.com/a6570ec5-ac77-427a-86d9-32cbecc62e37">Local Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

