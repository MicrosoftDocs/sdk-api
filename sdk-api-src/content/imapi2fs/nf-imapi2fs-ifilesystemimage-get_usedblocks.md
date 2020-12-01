---
UID: NF:imapi2fs.IFileSystemImage.get_UsedBlocks
title: IFileSystemImage::get_UsedBlocks (imapi2fs.h)
description: Retrieves the number of blocks in use.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_UsedBlocks method","IFileSystemImage.get_UsedBlocks","IFileSystemImage::get_UsedBlocks","get_UsedBlocks","get_UsedBlocks method [IMAPI]","get_UsedBlocks method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_usedblocks","imapi2fs/IFileSystemImage::get_UsedBlocks"]
old-location: imapi\ifilesystemimage_get_usedblocks.htm
tech.root: imapi
ms.assetid: 97f59440-112b-49ea-9f8e-97e8a831229d
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UsedBlocks method, IFileSystemImage.get_UsedBlocks, IFileSystemImage::get_UsedBlocks, get_UsedBlocks, get_UsedBlocks method [IMAPI], get_UsedBlocks method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_usedblocks, imapi2fs/IFileSystemImage::get_UsedBlocks
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
 - IFileSystemImage::get_UsedBlocks
 - imapi2fs/IFileSystemImage::get_UsedBlocks
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
 - IFileSystemImage.get_UsedBlocks
---

# IFileSystemImage::get_UsedBlocks


## -description

Retrieves the number of blocks in use.

## -parameters

### -param pVal [out]

Estimated number of blocks used in the file-system image.

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