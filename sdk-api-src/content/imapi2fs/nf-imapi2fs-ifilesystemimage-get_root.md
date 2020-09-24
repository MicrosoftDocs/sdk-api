---
UID: NF:imapi2fs.IFileSystemImage.get_Root
title: IFileSystemImage::get_Root (imapi2fs.h)
description: Retrieves the root directory item.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_Root method","IFileSystemImage.get_Root","IFileSystemImage::get_Root","get_Root","get_Root method [IMAPI]","get_Root method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_root","imapi2fs/IFileSystemImage::get_Root"]
old-location: imapi\ifilesystemimage_get_root.htm
tech.root: imapi
ms.assetid: 4b43468a-f02c-4806-9f65-529dc6d8f20a
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_Root method, IFileSystemImage.get_Root, IFileSystemImage::get_Root, get_Root, get_Root method [IMAPI], get_Root method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_root, imapi2fs/IFileSystemImage::get_Root
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
 - IFileSystemImage::get_Root
 - imapi2fs/IFileSystemImage::get_Root
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
 - IFileSystemImage.get_Root
---

# IFileSystemImage::get_Root


## -description

Retrieves the root directory item.

## -parameters

### -param pVal [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a> interface of the root directory item.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>