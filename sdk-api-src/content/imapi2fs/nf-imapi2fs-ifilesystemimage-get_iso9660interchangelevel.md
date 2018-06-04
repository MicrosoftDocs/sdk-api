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

# IFileSystemImage::get_ISO9660InterchangeLevel


## -description


Retrieves the ISO9660 compatibility level to use when creating the result image.


## -parameters




### -param pVal [out]

Identifies the interchange level of the ISO9660 file system. 


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
 




## -remarks



For a list of supported compatibility levels, call the <a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a>



<a href="https://msdn.microsoft.com/8bfb770a-5a69-4980-94e2-4a3f65caa645">IFileSystemImage::put_ISO9660InterchangeLevel</a>
 

 

