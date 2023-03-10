---
UID: NF:imapi2fs.IFsiItem.put_IsHidden
title: IFsiItem::put_IsHidden (imapi2fs.h)
description: Determines if the item's hidden attribute is set in the file system image. (Put)
helpviewer_keywords: ["IFsiItem interface [IMAPI]","put_IsHidden method","IFsiItem.put_IsHidden","IFsiItem::put_IsHidden","imapi.ifsiitem_put_ishidden","imapi2fs/IFsiItem::put_IsHidden","put_IsHidden","put_IsHidden method [IMAPI]","put_IsHidden method [IMAPI]","IFsiItem interface"]
old-location: imapi\ifsiitem_put_ishidden.htm
tech.root: imapi
ms.assetid: a437daea-af30-43e5-bb88-e59de8ba37c9
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],put_IsHidden method, IFsiItem.put_IsHidden, IFsiItem::put_IsHidden, imapi.ifsiitem_put_ishidden, imapi2fs/IFsiItem::put_IsHidden, put_IsHidden, put_IsHidden method [IMAPI], put_IsHidden method [IMAPI],IFsiItem interface
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
 - IFsiItem::put_IsHidden
 - imapi2fs/IFsiItem::put_IsHidden
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
 - IFsiItem.put_IsHidden
---

# IFsiItem::put_IsHidden


## -description

Determines if the item's hidden attribute is set in the file system image.

## -parameters

### -param newVal [in]

Set to VARIANT_TRUE to set the hidden attribute of the item in the file system image; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.

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
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_ishidden">IFsiItem::get_IsHidden</a>
