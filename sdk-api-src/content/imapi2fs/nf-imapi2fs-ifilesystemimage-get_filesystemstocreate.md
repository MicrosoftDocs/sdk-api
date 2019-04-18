---
UID: NF:imapi2fs.IFileSystemImage.get_FileSystemsToCreate
title: IFileSystemImage::get_FileSystemsToCreate (imapi2fs.h)
author: windows-sdk-content
description: Retrieves the types of file systems to create when generating the result stream.
old-location: imapi\ifilesystemimage_get_filesystemstocreate.htm
tech.root: imapi
ms.assetid: 7350de0b-683a-4363-9233-dbe40f637f2d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FileSystemsToCreate method, IFileSystemImage.get_FileSystemsToCreate, IFileSystemImage::get_FileSystemsToCreate, get_FileSystemsToCreate, get_FileSystemsToCreate method [IMAPI], get_FileSystemsToCreate method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_filesystemstocreate, imapi2fs/IFileSystemImage::get_FileSystemsToCreate
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.get_FileSystemsToCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

