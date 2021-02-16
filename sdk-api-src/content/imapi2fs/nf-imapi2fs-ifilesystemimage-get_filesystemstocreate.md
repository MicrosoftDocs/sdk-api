---
UID: NF:imapi2fs.IFileSystemImage.get_FileSystemsToCreate
title: IFileSystemImage::get_FileSystemsToCreate (imapi2fs.h)
description: Retrieves the types of file systems to create when generating the result stream.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_FileSystemsToCreate method","IFileSystemImage.get_FileSystemsToCreate","IFileSystemImage::get_FileSystemsToCreate","get_FileSystemsToCreate","get_FileSystemsToCreate method [IMAPI]","get_FileSystemsToCreate method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_filesystemstocreate","imapi2fs/IFileSystemImage::get_FileSystemsToCreate"]
old-location: imapi\ifilesystemimage_get_filesystemstocreate.htm
tech.root: imapi
ms.assetid: 7350de0b-683a-4363-9233-dbe40f637f2d
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FileSystemsToCreate method, IFileSystemImage.get_FileSystemsToCreate, IFileSystemImage::get_FileSystemsToCreate, get_FileSystemsToCreate, get_FileSystemsToCreate method [IMAPI], get_FileSystemsToCreate method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_filesystemstocreate, imapi2fs/IFileSystemImage::get_FileSystemsToCreate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemImage::get_FileSystemsToCreate
 - imapi2fs/IFileSystemImage::get_FileSystemsToCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.get_FileSystemsToCreate
---

# IFileSystemImage::get_FileSystemsToCreate


## -description

Retrieves the types of file systems to create when generating the result stream.

## -parameters

### -param pVal [out]

One or more file system types to create when generating the result stream. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

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

To specify the file system types, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">IFileSystemImage::put_FileSystemsToCreate</a> method. You could also call either <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaults">IFilesystemImage::ChooseImageDefaults</a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaultsformediatype">IFilesystemImage::ChooseImageDefaultsForMediaType</a> to have IMAPI choose the file system for you.

To retrieve a list of supported file system types, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemssupported">IFileSystemImage::get_FileSystemsSupported</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">IFileSystemImage::CreateResultImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">IFileSystemImage::put_FileSystemsToCreate</a>