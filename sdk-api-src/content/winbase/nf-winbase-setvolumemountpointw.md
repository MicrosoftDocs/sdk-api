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

# SetVolumeMountPointW function


## -description


Associates a volume with a drive letter or a directory on another volume.


## -parameters




### -param lpszVolumeMountPoint [in]

The user-mode path to be associated with the volume. This may be a drive letter (for example, "X:\") or a directory 
      on another volume (for example, "Y:\MountX\"). The string must end with a trailing backslash ('\').


### -param lpszVolumeName [in]

A volume <b>GUID</b> path for the volume. This string must be of the form 
      "\\?\Volume{<i>GUID</i>}\" where <i>GUID</i> is a <b>GUID</b> that identifies 
      the volume. The "\\?\" turns off path parsing and is ignored as part of the path, as discussed in 
      <a href="https://msdn.microsoft.com/f640f42d-a703-4e2e-a6d3-09cbe989cd11">Naming a Volume</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the <i>lpszVolumeMountPoint</i> parameter contains a path to a mounted folder, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_DIR_NOT_EMPTY</b>, even if the directory is empty.




## -remarks



When this function is used to associate a volume with a directory on another volume, the associated directory is called a <i>mounted folder</i>.

It is an error to associate a volume with a directory that has any files or subdirectories in it. This 
    error occurs for system and hidden directories as well as other directories, and it occurs for system and hidden 
    files.

When mounted folders are created on a volume on a clustered disk, they may be deleted unexpectedly under certain 
    circumstances. For information on how to create and configure mounted folders to ensure that this does not happen, 
    see <a href="Http://go.microsoft.com/fwlink/p/?linkid=169338">Cluster Disk and Drive Connection Problems</a>.

IIn Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
No

</td>
</tr>
</table>
 

SMB does not support volume management functions. For CsvFS a new mount point will not be replicated to the other nodes on the cluster.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/c97bfd10-66ff-41e1-ba3b-f98a019948d5">Creating a Mounted Folder</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b1a0a273-fa7f-4794-8b50-c74f00b0228d">DeleteVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

