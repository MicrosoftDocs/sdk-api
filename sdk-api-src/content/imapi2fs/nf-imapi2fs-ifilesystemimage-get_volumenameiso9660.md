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

# IFileSystemImage::get_VolumeNameISO9660


## -description


Retrieves the volume name for the ISO9660 system image.


## -parameters




### -param pVal [out]

String that contains the volume name for the ISO9660 system image. 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">IFileSystemImage::get_VolumeName</a>



<a href="https://msdn.microsoft.com/5300763d-9f2f-4562-bb5e-61fcf485b086">IFileSystemImage::get_VolumeNameJoliet</a>



<a href="https://msdn.microsoft.com/d034f8cb-38f5-42ab-8952-e4a76dc1f27d">IFileSystemImage::get_VolumeNameUDF</a>
 

 

