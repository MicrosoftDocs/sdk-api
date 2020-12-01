---
UID: NF:imapi2fs.IFileSystemImage.CreateDirectoryItem
title: IFileSystemImage::CreateDirectoryItem (imapi2fs.h)
description: Create a directory item with the specified name.
helpviewer_keywords: ["CreateDirectoryItem","CreateDirectoryItem method [IMAPI]","CreateDirectoryItem method [IMAPI]","IFileSystemImage interface","IFileSystemImage interface [IMAPI]","CreateDirectoryItem method","IFileSystemImage.CreateDirectoryItem","IFileSystemImage::CreateDirectoryItem","imapi.ifilesystemimage_createdirectoryitem","imapi2fs/IFileSystemImage::CreateDirectoryItem"]
old-location: imapi\ifilesystemimage_createdirectoryitem.htm
tech.root: imapi
ms.assetid: 27eadc99-46b6-40e1-91e0-b5c532536491
ms.date: 12/05/2018
ms.keywords: CreateDirectoryItem, CreateDirectoryItem method [IMAPI], CreateDirectoryItem method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],CreateDirectoryItem method, IFileSystemImage.CreateDirectoryItem, IFileSystemImage::CreateDirectoryItem, imapi.ifilesystemimage_createdirectoryitem, imapi2fs/IFileSystemImage::CreateDirectoryItem
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
 - IFileSystemImage::CreateDirectoryItem
 - imapi2fs/IFileSystemImage::CreateDirectoryItem
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
 - IFileSystemImage.CreateDirectoryItem
---

# IFileSystemImage::CreateDirectoryItem


## -description

Create a directory item with the specified name.

## -parameters

### -param name [in]

String that contains the name of the directory item to create.

### -param newItem [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a> interface of the new directory item.  When done, call the <b>IFsiDirectoryItem::Release</b> method to release the interface.

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

After setting properties on the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a> interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a> method on the parent directory item to add it to the file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>