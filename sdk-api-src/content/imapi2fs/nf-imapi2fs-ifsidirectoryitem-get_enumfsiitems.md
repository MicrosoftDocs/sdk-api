---
UID: NF:imapi2fs.IFsiDirectoryItem.get_EnumFsiItems
title: IFsiDirectoryItem::get_EnumFsiItems (imapi2fs.h)
description: Retrieves a list of child items contained within the directory in the file system image. (IFsiDirectoryItem.get_EnumFsiItems)
helpviewer_keywords: ["IFsiDirectoryItem interface [IMAPI]","get_EnumFsiItems method","IFsiDirectoryItem.get_EnumFsiItems","IFsiDirectoryItem::get_EnumFsiItems","get_EnumFsiItems","get_EnumFsiItems method [IMAPI]","get_EnumFsiItems method [IMAPI]","IFsiDirectoryItem interface","imapi.ifsidirectoryitem_get_enumfsiitems","imapi2fs/IFsiDirectoryItem::get_EnumFsiItems"]
old-location: imapi\ifsidirectoryitem_get_enumfsiitems.htm
tech.root: imapi
ms.assetid: 723f28ad-f77d-494f-9ae6-ba6120675cfd
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_EnumFsiItems method, IFsiDirectoryItem.get_EnumFsiItems, IFsiDirectoryItem::get_EnumFsiItems, get_EnumFsiItems, get_EnumFsiItems method [IMAPI], get_EnumFsiItems method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_enumfsiitems, imapi2fs/IFsiDirectoryItem::get_EnumFsiItems
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
 - IFsiDirectoryItem::get_EnumFsiItems
 - imapi2fs/IFsiDirectoryItem::get_EnumFsiItems
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
 - IFsiDirectoryItem.get_EnumFsiItems
---

# IFsiDirectoryItem::get_EnumFsiItems


## -description

Retrieves a list of child items contained within the directory in the file system image.

## -parameters

### -param NewEnum [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems">IEnumFsiItems</a> interface that contains a collection of the child directory and file items contained within the directory.

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
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

This property returns the same results as the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get__newenum">IFsiDirectoryItem::get__NewEnum</a> property and is meant for use by C/C++ applications.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems">IEnumFsiItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get__newenum">IFsiDirectoryItem::get__NewEnum</a>
