---
UID: NF:photoacquire.IPhotoAcquireItem.SetProperty
title: IPhotoAcquireItem::SetProperty (photoacquire.h)
description: The SetProperty method sets a property for an item.
helpviewer_keywords: ["IPhotoAcquireItem interface [Picture Acquisition]","SetProperty method","IPhotoAcquireItem.SetProperty","IPhotoAcquireItem::SetProperty","IPhotoAcquireItemSetProperty","SetProperty","SetProperty method [Picture Acquisition]","SetProperty method [Picture Acquisition]","IPhotoAcquireItem interface","photoacquire/IPhotoAcquireItem::SetProperty","picacq.iphotoacquireitem_setproperty"]
old-location: picacq\iphotoacquireitem_setproperty.htm
tech.root: picacq
ms.assetid: 24c8ee32-eb10-416f-81bd-ddccb0f81fd9
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireItem interface [Picture Acquisition],SetProperty method, IPhotoAcquireItem.SetProperty, IPhotoAcquireItem::SetProperty, IPhotoAcquireItemSetProperty, SetProperty, SetProperty method [Picture Acquisition], SetProperty method [Picture Acquisition],IPhotoAcquireItem interface, photoacquire/IPhotoAcquireItem::SetProperty, picacq.iphotoacquireitem_setproperty
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
 - IPhotoAcquireItem::SetProperty
 - photoacquire/IPhotoAcquireItem::SetProperty
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
 - IPhotoAcquireItem.SetProperty
---

# IPhotoAcquireItem::SetProperty


## -description

The <code>SetProperty</code> method sets a property for an item.

## -parameters

### -param key [in]

Specifies a key for the property to set.

### -param pv [in]

Pointer to a property variant containing the value to set the property to.

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

The property is stored in memory, but is not written to the file.

## -see-also

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getproperty">GetProperty</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>