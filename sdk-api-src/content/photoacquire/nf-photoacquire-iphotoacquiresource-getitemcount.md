---
UID: NF:photoacquire.IPhotoAcquireSource.GetItemCount
title: IPhotoAcquireSource::GetItemCount (photoacquire.h)
description: The GetItemCount method retrieves the number of items found by the InitializeItemList method.
helpviewer_keywords: ["GetItemCount","GetItemCount method [Picture Acquisition]","GetItemCount method [Picture Acquisition]","IPhotoAcquireSource interface","IPhotoAcquireSource interface [Picture Acquisition]","GetItemCount method","IPhotoAcquireSource.GetItemCount","IPhotoAcquireSource::GetItemCount","IPhotoAcquireSourceGetItemCount","photoacquire/IPhotoAcquireSource::GetItemCount","picacq.iphotoacquiresource_getitemcount"]
old-location: picacq\iphotoacquiresource_getitemcount.htm
tech.root: picacq
ms.assetid: f60538f2-f1b1-40bb-8663-ed93eede433e
ms.date: 12/05/2018
ms.keywords: GetItemCount, GetItemCount method [Picture Acquisition], GetItemCount method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetItemCount method, IPhotoAcquireSource.GetItemCount, IPhotoAcquireSource::GetItemCount, IPhotoAcquireSourceGetItemCount, photoacquire/IPhotoAcquireSource::GetItemCount, picacq.iphotoacquiresource_getitemcount
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
 - IPhotoAcquireSource::GetItemCount
 - photoacquire/IPhotoAcquireSource::GetItemCount
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
 - IPhotoAcquireSource.GetItemCount
---

# IPhotoAcquireSource::GetItemCount


## -description

The <code>GetItemCount</code> method retrieves the number of items found by the <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">InitializeItemList</a> method.

## -parameters

### -param pnItemCount [out]

Pointer to an integer value containing the item count.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed where a non-NULL pointer was expected.

</td>
</tr>
</table>

## -remarks

Before calling this method, call <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">InitializeItemList</a> to initialize the item list.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">IPhotoAcquireSource::InitializeItemList</a>