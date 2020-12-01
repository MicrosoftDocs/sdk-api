---
UID: NF:photoacquire.IPhotoAcquireItem.GetSubItemAt
title: IPhotoAcquireItem::GetSubItemAt (photoacquire.h)
description: The GetSubItemAt method retrieves a subitem of an item, given the index of the subitem.
helpviewer_keywords: ["GetSubItemAt","GetSubItemAt method [Picture Acquisition]","GetSubItemAt method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","GetSubItemAt method","IPhotoAcquireItem.GetSubItemAt","IPhotoAcquireItem::GetSubItemAt","IPhotoAcquireItemGetSubItemAt","photoacquire/IPhotoAcquireItem::GetSubItemAt","picacq.iphotoacquireitem_getsubitemat"]
old-location: picacq\iphotoacquireitem_getsubitemat.htm
tech.root: picacq
ms.assetid: 2fd410a0-20b5-4e16-9d36-89a14443c8bd
ms.date: 12/05/2018
ms.keywords: GetSubItemAt, GetSubItemAt method [Picture Acquisition], GetSubItemAt method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetSubItemAt method, IPhotoAcquireItem.GetSubItemAt, IPhotoAcquireItem::GetSubItemAt, IPhotoAcquireItemGetSubItemAt, photoacquire/IPhotoAcquireItem::GetSubItemAt, picacq.iphotoacquireitem_getsubitemat
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireItem::GetSubItemAt
 - photoacquire/IPhotoAcquireItem::GetSubItemAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireItem.GetSubItemAt
---

# IPhotoAcquireItem::GetSubItemAt


## -description

The <code>GetSubItemAt</code> method retrieves a subitem of an item, given the index of the subitem.

## -parameters

### -param nItemIndex [in]

Integer containing the index of the item.

### -param ppPhotoAcquireItem [out]

Returns the <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object at the given index.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

If no item is found at the given index, <i>ppPhotoAcquireItem</i> is set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>