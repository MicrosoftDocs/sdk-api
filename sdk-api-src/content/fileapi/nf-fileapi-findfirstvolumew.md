---
UID: NF:fileapi.FindFirstVolumeW
title: FindFirstVolumeW function
author: windows-sdk-content
description: Retrieves the name of a volume on a computer.
old-location: fs\findfirstvolume.htm
old-project: fileio
ms.assetid: 3eaf9903-ae20-47e7-b32c-943bf60e7bbd
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: FindFirstVolume, FindFirstVolume function [Files], FindFirstVolumeA, FindFirstVolumeW, _win32_findfirstvolume, base.findfirstvolume, fileapi/FindFirstVolume, fileapi/FindFirstVolumeA, fileapi/FindFirstVolumeW, fs.findfirstvolume, winbase/FindFirstVolume, winbase/FindFirstVolumeA, winbase/FindFirstVolumeW
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
req.unicode-ansi: FindFirstVolumeW (Unicode) and FindFirstVolumeA (ANSI)
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
 - API-Ms-Win-Core-File-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - FindFirstVolume
 - FindFirstVolumeA
 - FindFirstVolumeW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FindFirstVolumeW function


## -description


Retrieves the name of a volume on a computer. <b>FindFirstVolume</b> is used to begin scanning the volumes of a computer.


## -parameters




### -param lpszVolumeName [out]

A pointer to a buffer that receives a null-terminated string that specifies a volume 
      <b>GUID</b> path for the first volume that is found.


### -param cchBufferLength [in]

The length of the buffer to receive the volume <b>GUID</b> path, in 
      <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is a search handle used in a subsequent call to the 
       <a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a> and 
       <a href="https://msdn.microsoft.com/091a2f0c-df38-4fef-a926-3507545bb58d">FindVolumeClose</a> functions.

If the function fails to find any volumes, the return value is the 
       <b>INVALID_HANDLE_VALUE</b> error code. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>FindFirstVolume</b> function opens a volume search handle and returns 
    information about the first volume found on a computer. After the search handle is established, you can use the 
    <a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a> function to search for other volumes. When 
    the search handle is no longer needed, close it by using the 
    <a href="https://msdn.microsoft.com/091a2f0c-df38-4fef-a926-3507545bb58d">FindVolumeClose</a> function.

You should not assume any correlation between the order of the volumes that are returned by these functions 
    and the order of the volumes that are on the computer. In particular, do not assume any correlation between volume 
    order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.

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




<a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a>



<a href="https://msdn.microsoft.com/091a2f0c-df38-4fef-a926-3507545bb58d">FindVolumeClose</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

