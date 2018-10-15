---
UID: NF:winbase.FindVolumeMountPointClose
title: FindVolumeMountPointClose function
author: windows-sdk-content
description: Closes the specified mounted folder search handle.
old-location: fs\findvolumemountpointclose.htm
tech.root: FileIO
ms.assetid: f0f09a9d-e463-4457-9078-3d324fa8d4d6
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FindVolumeMountPointClose, FindVolumeMountPointClose function [Files], _win32_findvolumemountpointclose, base.findvolumemountpointclose, fs.findvolumemountpointclose, winbase/FindVolumeMountPointClose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - FindVolumeMountPointClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindVolumeMountPointClose function


## -description


Closes the specified mounted folder search handle. The 
    <a href="https://msdn.microsoft.com/2ac3c22d-b8dd-43d8-a7af-877b54e42d9d">FindFirstVolumeMountPoint</a> and 
<a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a>functions use this search handle to locate mounted folders on a specified volume.


## -parameters




### -param hFindVolumeMountPoint [in]

The mounted folder search handle to be closed. This handle must have been previously opened by the 
<a href="https://msdn.microsoft.com/2ac3c22d-b8dd-43d8-a7af-877b54e42d9d">FindFirstVolumeMountPoint</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the 
<b>FindVolumeMountPointClose</b> function is called, the handle <i>hFindVolumeMountPoint</i> cannot be used in subsequent calls to either 
<a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a> or 
<b>FindVolumeMountPointClose</b>.

The <a href="https://msdn.microsoft.com/2ac3c22d-b8dd-43d8-a7af-877b54e42d9d">FindFirstVolumeMountPoint</a>, <a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a>, and <b>FindVolumeMountPointClose</b> functions return paths to mounted folders for a specified volume. They do not return drive letters or volume GUID paths. For information about enumerating the volume GUID paths for a volume, see <a href="https://msdn.microsoft.com/f6590a46-2e09-472c-8231-bb24c9b0b5f6">Enumerating Volume GUID Paths</a>.

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
No

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
 

SMB does not support volume management functions. CsvFS does not support adding mount point on a CSV volume.




## -see-also




<a href="https://msdn.microsoft.com/2ac3c22d-b8dd-43d8-a7af-877b54e42d9d">FindFirstVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/299e2fed-74d8-4008-b593-981c52016532">FindNextVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume
    Management Functions</a>
 

 

