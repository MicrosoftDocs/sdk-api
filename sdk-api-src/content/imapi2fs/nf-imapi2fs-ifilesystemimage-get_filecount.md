---
UID: NF:imapi2fs.IFileSystemImage.get_FileCount
title: IFileSystemImage::get_FileCount (imapi2fs.h)
description: Retrieves the number of files in the file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_FileCount method","IFileSystemImage.get_FileCount","IFileSystemImage::get_FileCount","get_FileCount","get_FileCount method [IMAPI]","get_FileCount method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_filecount","imapi2fs/IFileSystemImage::get_FileCount"]
old-location: imapi\ifilesystemimage_get_filecount.htm
tech.root: imapi
ms.assetid: b2545f85-84c9-4f01-98d7-fd6b37fcda5a
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FileCount method, IFileSystemImage.get_FileCount, IFileSystemImage::get_FileCount, get_FileCount, get_FileCount method [IMAPI], get_FileCount method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_filecount, imapi2fs/IFileSystemImage::get_FileCount
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
 - IFileSystemImage::get_FileCount
 - imapi2fs/IFileSystemImage::get_FileCount
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
 - IFileSystemImage.get_FileCount
---

# IFileSystemImage::get_FileCount


## -description

Retrieves the number of files in the file system image.

## -parameters

### -param pVal [out]

Number of files in the file system image.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>