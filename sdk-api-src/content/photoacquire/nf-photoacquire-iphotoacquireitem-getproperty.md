---
UID: NF:photoacquire.IPhotoAcquireItem.GetProperty
title: IPhotoAcquireItem::GetProperty (photoacquire.h)
description: The GetProperty method retrieves the value of a property of an item.
helpviewer_keywords: ["GetProperty","GetProperty method [Picture Acquisition]","GetProperty method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","GetProperty method","IPhotoAcquireItem.GetProperty","IPhotoAcquireItem::GetProperty","IPhotoAcquireItemGetProperty","photoacquire/IPhotoAcquireItem::GetProperty","picacq.iphotoacquireitem_getproperty"]
old-location: picacq\iphotoacquireitem_getproperty.htm
tech.root: picacq
ms.assetid: 47ee6a23-5a0b-4f45-b278-9ebbeebf4fbb
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Picture Acquisition], GetProperty method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetProperty method, IPhotoAcquireItem.GetProperty, IPhotoAcquireItem::GetProperty, IPhotoAcquireItemGetProperty, photoacquire/IPhotoAcquireItem::GetProperty, picacq.iphotoacquireitem_getproperty
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
 - IPhotoAcquireItem::GetProperty
 - photoacquire/IPhotoAcquireItem::GetProperty
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
 - IPhotoAcquireItem.GetProperty
---

# IPhotoAcquireItem::GetProperty


## -description

The <code>GetProperty</code> method retrieves the value of a property of an item.

## -parameters

### -param key [in]

Specifies a key for the property.

### -param pv [out]

Pointer to a property variant containing the property value.

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

For an item that is a shell object, this method will defer to the <b>IPropertyStore</b> object provided by the item if the property hasn't been set or updated using <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-setproperty">SetProperty</a>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-setproperty">SetProperty</a>