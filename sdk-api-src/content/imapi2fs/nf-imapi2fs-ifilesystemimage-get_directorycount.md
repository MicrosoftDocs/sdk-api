---
UID: NF:imapi2fs.IFileSystemImage.get_DirectoryCount
title: IFileSystemImage::get_DirectoryCount (imapi2fs.h)
description: Retrieves the number of directories in the file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_DirectoryCount method","IFileSystemImage.get_DirectoryCount","IFileSystemImage::get_DirectoryCount","get_DirectoryCount","get_DirectoryCount method [IMAPI]","get_DirectoryCount method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_directorycount","imapi2fs/IFileSystemImage::get_DirectoryCount"]
old-location: imapi\ifilesystemimage_get_directorycount.htm
tech.root: imapi
ms.assetid: fc8e0606-8662-441f-b244-7d6b0be4c4e7
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_DirectoryCount method, IFileSystemImage.get_DirectoryCount, IFileSystemImage::get_DirectoryCount, get_DirectoryCount, get_DirectoryCount method [IMAPI], get_DirectoryCount method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_directorycount, imapi2fs/IFileSystemImage::get_DirectoryCount
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
 - IFileSystemImage::get_DirectoryCount
 - imapi2fs/IFileSystemImage::get_DirectoryCount
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
 - IFileSystemImage.get_DirectoryCount
---

# IFileSystemImage::get_DirectoryCount


## -description

Retrieves the number of directories in the file system image.

## -parameters

### -param pVal [out]

Number of directories in the file system image.

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