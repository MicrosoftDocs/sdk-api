---
UID: NF:photoacquire.IPhotoAcquireItem.CanDelete
title: IPhotoAcquireItem::CanDelete (photoacquire.h)
description: The CanDelete method indicates whether an item may be deleted.
helpviewer_keywords: ["CanDelete","CanDelete method [Picture Acquisition]","CanDelete method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","CanDelete method","IPhotoAcquireItem.CanDelete","IPhotoAcquireItem::CanDelete","IPhotoAcquireItemCanDelete","photoacquire/IPhotoAcquireItem::CanDelete","picacq.iphotoacquireitem_candelete"]
old-location: picacq\iphotoacquireitem_candelete.htm
tech.root: picacq
ms.assetid: df0acbed-0352-4591-8908-f0dda1da25dd
ms.date: 12/05/2018
ms.keywords: CanDelete, CanDelete method [Picture Acquisition], CanDelete method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],CanDelete method, IPhotoAcquireItem.CanDelete, IPhotoAcquireItem::CanDelete, IPhotoAcquireItemCanDelete, photoacquire/IPhotoAcquireItem::CanDelete, picacq.iphotoacquireitem_candelete
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
 - IPhotoAcquireItem::CanDelete
 - photoacquire/IPhotoAcquireItem::CanDelete
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
 - IPhotoAcquireItem.CanDelete
---

# IPhotoAcquireItem::CanDelete


## -description

The <code>CanDelete</code> method indicates whether an item may be deleted.

## -parameters

### -param pfCanDelete [out]

Pointer to a flag that, when set to <b>TRUE</b>, indicates that the item can be deleted.

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

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>