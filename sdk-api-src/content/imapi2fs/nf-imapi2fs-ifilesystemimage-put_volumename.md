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

# IFileSystemImage::put_VolumeName


## -description


Sets the volume name for this file system image. 


## -parameters




### -param newVal [in]

String that contains the volume name for this file system image.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_VOLUME_NAME</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>
 




## -remarks



The string is limited to 15 characters. For ISO 9660 discs, the volume name can use the following characters:

<ul>
<li>"A" through "Z"</li>
<li>"0" through "9"</li>
<li>"_" (underscore)</li>
</ul>
For Joliet and UDF discs, the volume name can use the following characters:

<ul>
<li>"a" through "z"</li>
<li>"A" through "Z"</li>
<li>"0" through "9"</li>
<li>"." (period)</li>
<li>"_" (underscore)</li>
</ul>
If you do not specify a volume name, a default volume name is generated using the system date and time when the result object is created. 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/57d66dd3-2525-4102-bba7-00bad76a3d9c">IFileSystemImage::get_ImportedVolumeName</a>



<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">IFileSystemImage::get_VolumeName</a>
 

 

