---
UID: NF:fileapi.FindVolumeClose
title: FindVolumeClose function
author: windows-sdk-content
description: Closes the specified volume search handle.
old-location: fs\findvolumeclose.htm
old-project: FileIO
ms.assetid: 091a2f0c-df38-4fef-a926-3507545bb58d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FindVolumeClose, FindVolumeClose function [Files], _win32_findvolumeclose, base.findvolumeclose, fileapi/FindVolumeClose, fs.findvolumeclose, winbase/FindVolumeClose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
-	FindVolumeClose
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FindVolumeClose function


## -description


Closes the specified volume search handle. The <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> and 
<a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a> functions use this search handle to locate volumes.


## -parameters




### -param hFindVolume [in]

The volume search handle to be closed. This handle must have been previously opened by the 
<a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the 
<b>FindVolumeClose</b> function is called, the handle <i>hFindVolume</i> cannot be used in subsequent calls to either 
<a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a> or 
<b>FindVolumeClose</b>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

SMB does not support volume management functions.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/a9ee8cc8-fa62-4fc9-aa69-35ee98afe417">Displaying Volume Paths</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a>



<a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

