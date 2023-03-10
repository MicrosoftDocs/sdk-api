---
UID: NF:imapi2fs.IFsiDirectoryItem.get__NewEnum
title: IFsiDirectoryItem::get__NewEnum (imapi2fs.h)
description: Retrieves a list of child items contained within the directory in the file system image. (IFsiDirectoryItem.get__NewEnum)
helpviewer_keywords: ["IFsiDirectoryItem interface [IMAPI]","get__NewEnum method","IFsiDirectoryItem.get__NewEnum","IFsiDirectoryItem::get__NewEnum","get__NewEnum","get__NewEnum method [IMAPI]","get__NewEnum method [IMAPI]","IFsiDirectoryItem interface","imapi.ifsidirectoryitem_get__newenum","imapi2fs/IFsiDirectoryItem::get__NewEnum"]
old-location: imapi\ifsidirectoryitem_get__newenum.htm
tech.root: imapi
ms.assetid: 08ffc4dd-7001-4a89-a58e-a12e21600172
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get__NewEnum method, IFsiDirectoryItem.get__NewEnum, IFsiDirectoryItem::get__NewEnum, get__NewEnum, get__NewEnum method [IMAPI], get__NewEnum method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get__newenum, imapi2fs/IFsiDirectoryItem::get__NewEnum
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
 - IFsiDirectoryItem::get__NewEnum
 - imapi2fs/IFsiDirectoryItem::get__NewEnum
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
 - IFsiDirectoryItem.get__NewEnum
---

# IFsiDirectoryItem::get__NewEnum


## -description

Retrieves a list of child items contained within the directory in the file system image.

## -parameters

### -param NewEnum [out]

An <b>IEnumVariant</b> interface that you use to enumerate the child items contained within the directory. The items of the enumeration are variants whose type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to retrieve the path to the child item.

## -returns

S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements. The <i>celt</i> and <i>pceltFetched</i> parameters are defined by <b>IEnumVariant</b>.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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

The enumeration is a snapshot of the children contained in the directory at the time of the call and will not reflect children that are added and removed. 

To retrieve a single item, see the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_item">IFsiDirectoryItem::get_Item</a> property.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_enumfsiitems">IFsiDirectoryItem::get_EnumFsiItems</a>
