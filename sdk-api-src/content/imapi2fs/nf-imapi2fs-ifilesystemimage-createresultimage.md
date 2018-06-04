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

# IFileSystemImage::CreateResultImage


## -description


Create the result object that contains the file system and file data.


## -parameters




### -param resultStream [out]

An <a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a> interface of the image result.

Client applications can stream the image to media or other long-term storage devices, such as disk drives.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -remarks



 Currently, <b>IFileSystemImage::CreateResultImage</b> will require disc media access as a result of  a previous <a href="https://msdn.microsoft.com/381be283-c877-44f0-9d96-b9e80a6aeec8">IFileSystemImage::IdentifyFileSystemsOnDisc</a> method call. To resolve this issue, it is recommended that another  <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> object be created specifically for the <b>IFileSystemImage::IdentifyFileSystemsOnDisc</b> operation.

The resulting stream can be saved as an ISO file if the file system is generated in a single session and has a start address of zero.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/7350de0b-683a-4363-9233-dbe40f637f2d">IFileSystemImage::get_FileSystemsToCreate</a>



<a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a>



<a href="https://msdn.microsoft.com/9211b8af-9331-4d0d-a6f5-f52f8db42e8c">IFilesystemImage::ChooseImageDefaults</a>



<a href="https://msdn.microsoft.com/1d327da0-d0b3-4fcf-9773-ff5ea1eeea1c">IFilesystemImage::ChooseImageDefaultsForMediaType</a>
 

 

