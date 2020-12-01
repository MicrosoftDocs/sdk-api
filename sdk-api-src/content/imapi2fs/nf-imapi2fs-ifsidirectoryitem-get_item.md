---
UID: NF:imapi2fs.IFsiDirectoryItem.get_Item
title: IFsiDirectoryItem::get_Item (imapi2fs.h)
description: Retrieves the specified directory or file item from file system image.
helpviewer_keywords: ["IFsiDirectoryItem interface [IMAPI]","get_Item method","IFsiDirectoryItem.get_Item","IFsiDirectoryItem::get_Item","get_Item","get_Item method [IMAPI]","get_Item method [IMAPI]","IFsiDirectoryItem interface","imapi.ifsidirectoryitem_get_item","imapi2fs/IFsiDirectoryItem::get_Item"]
old-location: imapi\ifsidirectoryitem_get_item.htm
tech.root: imapi
ms.assetid: 8ea5219c-a12f-43a3-a67b-16cd0e6d2bac
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_Item method, IFsiDirectoryItem.get_Item, IFsiDirectoryItem::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_item, imapi2fs/IFsiDirectoryItem::get_Item
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
 - IFsiDirectoryItem::get_Item
 - imapi2fs/IFsiDirectoryItem::get_Item
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
 - IFsiDirectoryItem.get_Item
---

# IFsiDirectoryItem::get_Item


## -description

Retrieves the specified directory or file item from file system image.

## -parameters

### -param path [in]

String that contains the path to the item to retrieve.

### -param item [out]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a> interface of the requested directory or file item.

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
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
Path '%1!s!' is badly formed or contains invalid characters.

Value: 0xC0AAB110

</td>
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
<dt><b>IMAPI_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Cannot find item <i>%1!ls!</i> in FileSystemImage hierarchy.

Value: 0xC0AAB118

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

To determine whether the item is a file item or directory item, call the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem::QueryInterface</a>  method passing __uuidof(IFsiDirectoryItem) as the interface identifier. If the call succeeds, the item is a directory item; otherwise, the item is a file item.

To enumerate all children, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get__newenum">IFsiDirectoryItem::get__NewEnum</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



IFsiFileItem