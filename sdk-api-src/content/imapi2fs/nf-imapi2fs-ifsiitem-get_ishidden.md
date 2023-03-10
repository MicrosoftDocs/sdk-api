---
UID: NF:imapi2fs.IFsiItem.get_IsHidden
title: IFsiItem::get_IsHidden (imapi2fs.h)
description: Determines if the item's hidden attribute is set in the file system image. (Get)
helpviewer_keywords: ["IFsiItem interface [IMAPI]","get_IsHidden method","IFsiItem.get_IsHidden","IFsiItem::get_IsHidden","get_IsHidden","get_IsHidden method [IMAPI]","get_IsHidden method [IMAPI]","IFsiItem interface","imapi.ifsiitem_get_ishidden","imapi2fs/IFsiItem::get_IsHidden"]
old-location: imapi\ifsiitem_get_ishidden.htm
tech.root: imapi
ms.assetid: 1aec5bbc-d602-40c1-80e4-cad9dd8a2ab5
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],get_IsHidden method, IFsiItem.get_IsHidden, IFsiItem::get_IsHidden, get_IsHidden, get_IsHidden method [IMAPI], get_IsHidden method [IMAPI],IFsiItem interface, imapi.ifsiitem_get_ishidden, imapi2fs/IFsiItem::get_IsHidden
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
 - IFsiItem::get_IsHidden
 - imapi2fs/IFsiItem::get_IsHidden
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
 - IFsiItem.get_IsHidden
---

# IFsiItem::get_IsHidden


## -description

Determines if the item's hidden attribute is set in the file system image.

## -parameters

### -param pVal [out]

Is VARIANT_TRUE if the hidden attribute of the item is marked in the file system image; otherwise, VARIANT_FALSE.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_ishidden">IFsiItem::put_IsHidden</a>
