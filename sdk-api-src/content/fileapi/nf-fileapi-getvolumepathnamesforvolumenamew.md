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

# GetVolumePathNamesForVolumeNameW function


## -description


Retrieves a list of drive letters and mounted folder paths for the specified volume.


## -parameters




### -param lpszVolumeName [in]

A volume <b>GUID</b> path for the volume. A volume <b>GUID</b> 
      path is of the form 
      "\\?\Volume{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}\".


### -param lpszVolumePathNames [out]

A pointer to a buffer that receives the list of drive letters and mounted folder paths. The list is an 
      array of null-terminated strings terminated by an additional <b>NULL</b> character. If the 
      buffer is not large enough to hold the complete list, the buffer holds as much of the list as possible.


### -param cchBufferLength [in]

The length of the <i>lpszVolumePathNames</i> buffer, in 
      <b>TCHARs</b>, including all <b>NULL</b> characters.


### -param lpcchReturnLength [out]

If the call is successful, this parameter is the number of <b>TCHARs</b> copied to 
      the <i>lpszVolumePathNames</i> buffer. Otherwise, this parameter is the size of the buffer 
      required to hold the complete list, in <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the buffer is not large enough to 
       hold the complete list, the error code is <b>ERROR_MORE_DATA</b> and the 
       <i>lpcchReturnLength</i> parameter receives the required buffer size.




## -remarks



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




<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

