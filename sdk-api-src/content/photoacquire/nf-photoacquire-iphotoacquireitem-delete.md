---
UID: NF:photoacquire.IPhotoAcquireItem.Delete
title: IPhotoAcquireItem::Delete (photoacquire.h)
description: The Delete method deletes an item.
helpviewer_keywords: ["Delete","Delete method [Picture Acquisition]","Delete method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","Delete method","IPhotoAcquireItem.Delete","IPhotoAcquireItem::Delete","IPhotoAcquireItemDelete","photoacquire/IPhotoAcquireItem::Delete","picacq.iphotoacquireitem_delete"]
old-location: picacq\iphotoacquireitem_delete.htm
tech.root: picacq
ms.assetid: e1ffe49b-b7d6-46ae-b83b-8d8487bd7b24
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Picture Acquisition], Delete method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],Delete method, IPhotoAcquireItem.Delete, IPhotoAcquireItem::Delete, IPhotoAcquireItemDelete, photoacquire/IPhotoAcquireItem::Delete, picacq.iphotoacquireitem_delete
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
 - IPhotoAcquireItem::Delete
 - photoacquire/IPhotoAcquireItem::Delete
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
 - IPhotoAcquireItem.Delete
---

# IPhotoAcquireItem::Delete


## -description

The <code>Delete</code> method deletes an item.



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

To determine whether an item may be deleted, call <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-candelete">CanDelete</a> first.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-candelete">IPhotoAcquireItem::CanDelete</a>
