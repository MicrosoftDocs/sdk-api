---
UID: NF:imapi2fs.IFileSystemImage.GetDefaultFileSystemForImport
title: IFileSystemImage::GetDefaultFileSystemForImport
author: windows-driver-content
description: Retrieves the file system to import by default.
old-location: imapi\ifilesystemimage_getdefaultfilesystemforimport.htm
old-project: imapi
ms.assetid: bbac5b93-669f-45ea-9a3d-e2dd7f8bdcf6
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetDefaultFileSystemForImport, GetDefaultFileSystemForImport method [IMAPI], GetDefaultFileSystemForImport method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],GetDefaultFileSystemForImport method, IFileSystemImage.GetDefaultFileSystemForImport, IFileSystemImage::GetDefaultFileSystemForImport, imapi.ifilesystemimage_getdefaultfilesystemforimport, imapi2fs/IFileSystemImage::GetDefaultFileSystemForImport
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
-	IFileSystemImage.GetDefaultFileSystemForImport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::GetDefaultFileSystemForImport


## -description


Retrieves the file system to import by default.


## -parameters




### -param fileSystems [in]

One or more file system values. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


### -param importDefault [out]

A single file system value that identifies the default file system.  The value is one of the file systems specified in <i>fileSystems</i>


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



Use this method to identify the default file system to use with <a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>.

To identify the supported file systems, call the <a href="https://msdn.microsoft.com/73bf563b-ad8f-4afe-95c6-3bac3c4dadba">IFileSystemImage::get_FileSystemsSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a>



<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>



<a href="https://msdn.microsoft.com/73bf563b-ad8f-4afe-95c6-3bac3c4dadba">IFileSystemImage::get_FileSystemsSupported</a>
 

 

