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

# IFileSystemImage::put_ISO9660InterchangeLevel


## -description


Sets the ISO9660 compatibility level of the file system image.


## -parameters




### -param newVal [in]

ISO9660 compatibility level of the file system image.


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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>
 




## -remarks



To determine the supported compatibility levels, call the <a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a> method.

This property is meaningful only if you specified FsiFileSystemISO9660 when calling <a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a>.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/9536444b-60e4-456f-b6d8-07cf9a6f7848">IFileSystemImage::get_ISO9660InterchangeLevel</a>



<a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a>
 

 

