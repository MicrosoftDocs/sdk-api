---
UID: NF:imapi2fs.IFileSystemImage.GetDefaultFileSystemForImport
title: IFileSystemImage::GetDefaultFileSystemForImport (imapi2fs.h)
description: Retrieves the file system to import by default.
helpviewer_keywords: ["GetDefaultFileSystemForImport","GetDefaultFileSystemForImport method [IMAPI]","GetDefaultFileSystemForImport method [IMAPI]","IFileSystemImage interface","IFileSystemImage interface [IMAPI]","GetDefaultFileSystemForImport method","IFileSystemImage.GetDefaultFileSystemForImport","IFileSystemImage::GetDefaultFileSystemForImport","imapi.ifilesystemimage_getdefaultfilesystemforimport","imapi2fs/IFileSystemImage::GetDefaultFileSystemForImport"]
old-location: imapi\ifilesystemimage_getdefaultfilesystemforimport.htm
tech.root: imapi
ms.assetid: bbac5b93-669f-45ea-9a3d-e2dd7f8bdcf6
ms.date: 12/05/2018
ms.keywords: GetDefaultFileSystemForImport, GetDefaultFileSystemForImport method [IMAPI], GetDefaultFileSystemForImport method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],GetDefaultFileSystemForImport method, IFileSystemImage.GetDefaultFileSystemForImport, IFileSystemImage::GetDefaultFileSystemForImport, imapi.ifilesystemimage_getdefaultfilesystemforimport, imapi2fs/IFileSystemImage::GetDefaultFileSystemForImport
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
 - IFileSystemImage::GetDefaultFileSystemForImport
 - imapi2fs/IFileSystemImage::GetDefaultFileSystemForImport
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
 - IFileSystemImage.GetDefaultFileSystemForImport
---

# IFileSystemImage::GetDefaultFileSystemForImport


## -description

Retrieves the file system to import by default.

## -parameters

### -param fileSystems [in]

One or more file system values. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

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

Use this method to identify the default file system to use with <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">IFileSystemImage::ImportFileSystem</a>.

To identify the supported file systems, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemssupported">IFileSystemImage::get_FileSystemsSupported</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">IFileSystemImage::ImportFileSystem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemssupported">IFileSystemImage::get_FileSystemsSupported</a>