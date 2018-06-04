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

# SetVolumeLabelA function


## -description


Sets the label of a file system volume.


## -parameters




### -param lpRootPathName [in, optional]

A pointer to a string that contains the volume's drive letter (for example, X:\) or the path 
      of a mounted folder that is associated with the volume (for example, Y:\MountX\). The string must 
      end with a trailing backslash ('\'). If this parameter is <b>NULL</b>, the root of the 
      current directory is used.


### -param lpVolumeName [in, optional]

A pointer to a string that contains the new label for the volume. If this parameter is 
      <b>NULL</b>, the function deletes any existing label from the specified volume and does not 
      assign a new label.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The maximum volume label length is 32 characters.

<b>FAT filesystems:  </b>The maximum volume label length is 11 characters.

A label is a user-friendly name that a user assigns to a volume to make it easier to recognize. A volume can 
    have a label, a drive letter, both, or neither. For more information, see 
    <a href="https://msdn.microsoft.com/f640f42d-a703-4e2e-a6d3-09cbe989cd11">Naming a Volume</a>.

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




## -see-also




<a href="https://msdn.microsoft.com/c80a38e1-319e-4f15-8c8a-9d29075e1709">GetVolumeInformation</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

