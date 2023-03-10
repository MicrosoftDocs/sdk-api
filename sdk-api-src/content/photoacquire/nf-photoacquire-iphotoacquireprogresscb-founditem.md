---
UID: NF:photoacquire.IPhotoAcquireProgressCB.FoundItem
title: IPhotoAcquireProgressCB::FoundItem (photoacquire.h)
description: The FoundItem method provides extended functionality each time an item is found during enumeration of items from the device.
helpviewer_keywords: ["FoundItem","FoundItem method [Picture Acquisition]","FoundItem method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB","IPhotoAcquireProgressCB interface [Picture Acquisition]","FoundItem method","IPhotoAcquireProgressCB.FoundItem","IPhotoAcquireProgressCB::FoundItem","photoacquire/IPhotoAcquireProgressCB::FoundItem","picacq.iphotoacquireprogresscb_founditem"]
old-location: picacq\iphotoacquireprogresscb_founditem.htm
tech.root: picacq
ms.assetid: b80fb2f2-57b7-4333-891e-32eba0347a17
ms.date: 12/05/2018
ms.keywords: FoundItem, FoundItem method [Picture Acquisition], FoundItem method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB, IPhotoAcquireProgressCB interface [Picture Acquisition],FoundItem method, IPhotoAcquireProgressCB.FoundItem, IPhotoAcquireProgressCB::FoundItem, photoacquire/IPhotoAcquireProgressCB::FoundItem, picacq.iphotoacquireprogresscb_founditem
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
 - IPhotoAcquireProgressCB::FoundItem
 - photoacquire/IPhotoAcquireProgressCB::FoundItem
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
 - IPhotoAcquireProgressCB.FoundItem
---

# IPhotoAcquireProgressCB::FoundItem


## -description

The <code>FoundItem</code> method provides extended functionality each time an item is found during enumeration of items from the device. This method can be used to exclude an item from the list of items to acquire. The application provides the implementation of the <code>FoundItem</code> method.

## -parameters

### -param pPhotoAcquireItem [in]

Pointer to the found <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Exclude this item from the list of files to acquire.

</td>
</tr>
</table>

## -remarks

Return S_FALSE to exclude the item from the results of the enumeration. This would allow the caller to exclude videos or camera raw files, for instance.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>