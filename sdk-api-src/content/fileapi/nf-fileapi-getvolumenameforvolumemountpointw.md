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

# GetVolumeNameForVolumeMountPointW function


## -description


Retrieves a volume <b>GUID</b> path for the volume that is associated with the specified volume mount point (
    drive letter, volume <b>GUID</b> path, or mounted folder).


## -parameters




### -param lpszVolumeMountPoint [in]

A pointer to a string that contains the path of a mounted folder (for example, "Y:\MountX\") or a drive letter (for example, "X:\"). The string must end with a trailing backslash ('\').


### -param lpszVolumeName [out]

A pointer to a string that receives the volume <b>GUID</b> path. This path is of the form "\\?\Volume{<i>GUID</i>}\" where <i>GUID</i> is a <b>GUID</b> that identifies the volume. If there is more than one volume <b>GUID</b> path for the volume, only the first one in the mount manager's cache is returned.


### -param cchBufferLength [in]

The length of the output buffer, in <b>TCHARs</b>. A reasonable size for the buffer to accommodate the largest possible volume <b>GUID</b> path is 50 characters.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Use 
<b>GetVolumeNameForVolumeMountPoint</b> to obtain a volume <b>GUID</b> path for use with functions such as <a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a> and <a href="https://msdn.microsoft.com/2ac3c22d-b8dd-43d8-a7af-877b54e42d9d">FindFirstVolumeMountPoint</a> that require a volume <b>GUID</b> path as an input parameter. For more information about volume <b>GUID</b> paths, see 
<a href="https://msdn.microsoft.com/f640f42d-a703-4e2e-a6d3-09cbe989cd11">Naming A Volume</a>.

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
No

</td>
</tr>
</table>
 

SMB does not support volume management functions.

Mount points aren't supported by ReFS volumes.




## -see-also




<a href="https://msdn.microsoft.com/b1a0a273-fa7f-4794-8b50-c74f00b0228d">DeleteVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

