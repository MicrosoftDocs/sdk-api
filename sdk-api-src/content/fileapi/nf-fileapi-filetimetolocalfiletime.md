---
UID: NF:fileapi.FileTimeToLocalFileTime
title: FileTimeToLocalFileTime function
author: windows-sdk-content
description: Converts a file time to a local file time.
old-location: base\filetimetolocalfiletime.htm
old-project: SysInfo
ms.assetid: 58dfce16-2d7f-4db5-9f84-5dd651d26745
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: FileTimeToLocalFileTime, FileTimeToLocalFileTime function, _win32_filetimetolocalfiletime, base.filetimetolocalfiletime, fileapi/FileTimeToLocalFileTime, winbase/FileTimeToLocalFileTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	FileTimeToLocalFileTime
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FileTimeToLocalFileTime function


## -description


Converts a file time to a local file time.


## -parameters




### -param lpFileTime [in]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the UTC-based file time to be converted into a local file time.


### -param lpLocalFileTime [out]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to receive the converted local file time. This parameter cannot be the same as the <i>lpFileTime</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To account for daylight saving time when converting a file time to a local time, use the following sequence of functions in place of using <b>FileTimeToLocalFileTime</b>:
    
                

<ol>
<li>
<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f3a87ec2-67a0-418f-af6e-6c0b5547cffb">SystemTimeToTzSpecificLocalTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/491e4724-8e6f-4155-b427-15cd7968e2da">LocalFileTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

