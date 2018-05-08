---
UID: NF:imapi2fs.IFileSystemImage.get_FileSystemsSupported
title: IFileSystemImage::get_FileSystemsSupported
author: windows-driver-content
description: Retrieves the list of file system types that a client can use to build a file system image.
old-location: imapi\ifilesystemimage_get_filesystemssupported.htm
old-project: imapi
ms.assetid: 73bf563b-ad8f-4afe-95c6-3bac3c4dadba
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FileSystemsSupported method, IFileSystemImage.get_FileSystemsSupported, IFileSystemImage::get_FileSystemsSupported, get_FileSystemsSupported, get_FileSystemsSupported method [IMAPI], get_FileSystemsSupported method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_filesystemssupported, imapi2fs/IFileSystemImage::get_FileSystemsSupported
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.get_FileSystemsSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_FileSystemsSupported


## -description


Retrieves the list of file system types that a client can use to build a file system image.


## -parameters




### -param pVal [out]

One or more file system types that a client can use to build a file system image. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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



<a href="https://msdn.microsoft.com/bbac5b93-669f-45ea-9a3d-e2dd7f8bdcf6">IFileSystemImage::GetDefaultFileSystemForImport</a>



<a href="https://msdn.microsoft.com/7350de0b-683a-4363-9233-dbe40f637f2d">IFileSystemImage::get_FileSystemsToCreate</a>



<a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">IFileSystemImage::put_FileSystemsToCreate</a>
 

 

