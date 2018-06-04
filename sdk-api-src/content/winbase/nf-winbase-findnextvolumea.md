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

# FindNextVolumeA function


## -description


Continues a volume search started by a call to the 
    <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> function. <b>FindNextVolume</b> finds one volume per call.


## -parameters




### -param hFindVolume [in]

The volume search handle returned by a previous call to the 
      <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> function.


### -param lpszVolumeName [out]

A pointer to a string that receives the volume <b>GUID</b> path that is found.


### -param cchBufferLength [in]

The length of the buffer that receives the volume <b>GUID</b> path, in 
      <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If no matching files can be found, the 
       <b>GetLastError</b> function returns the 
       <b>ERROR_NO_MORE_FILES</b> error code. In that case, close the search with the 
       <a href="https://msdn.microsoft.com/091a2f0c-df38-4fef-a926-3507545bb58d">FindVolumeClose</a> function.




## -remarks



After the search handle is established by calling 
    <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a>, you can use the 
    <b>FindNextVolume</b> function to search for other volumes.

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




<a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a>



<a href="https://msdn.microsoft.com/091a2f0c-df38-4fef-a926-3507545bb58d">FindVolumeClose</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

