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

# IFileSystemImage::get_FileSystemsToCreate


## -description


Retrieves the types of file systems to create when generating the result stream.


## -parameters




### -param pVal [out]

One or more file system types to create when generating the result stream. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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



To specify the file system types, call the <a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a> method. You could also call either <a href="https://msdn.microsoft.com/9211b8af-9331-4d0d-a6f5-f52f8db42e8c">IFilesystemImage::ChooseImageDefaults</a> or <a href="https://msdn.microsoft.com/1d327da0-d0b3-4fcf-9773-ff5ea1eeea1c">IFilesystemImage::ChooseImageDefaultsForMediaType</a> to have IMAPI choose the file system for you.

To retrieve a list of supported file system types, call the <a href="https://msdn.microsoft.com/73bf563b-ad8f-4afe-95c6-3bac3c4dadba">IFileSystemImage::get_FileSystemsSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/6f7d2438-5c80-4461-8b48-646f0ca44498">IFileSystemImage::CreateResultImage</a>



<a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a>
 

 

