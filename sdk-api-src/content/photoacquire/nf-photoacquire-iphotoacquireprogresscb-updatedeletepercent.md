---
UID: NF:photoacquire.IPhotoAcquireProgressCB.UpdateDeletePercent
title: IPhotoAcquireProgressCB::UpdateDeletePercent (photoacquire.h)
description: The UpdateDeletePercent method provides extended functionality when the percentage of items deleted changes. The application provides the implementation of the UpdateDeletePercent method.
helpviewer_keywords: ["IPhotoAcquireProgressCB interface [Picture Acquisition]","UpdateDeletePercent method","IPhotoAcquireProgressCB.UpdateDeletePercent","IPhotoAcquireProgressCB::UpdateDeletePercent","IPhotoAcquireProgressCBUpdateDeletePercent","UpdateDeletePercent","UpdateDeletePercent method [Picture Acquisition]","UpdateDeletePercent method [Picture Acquisition]","IPhotoAcquireProgressCB interface","photoacquire/IPhotoAcquireProgressCB::UpdateDeletePercent","picacq.iphotoacquireprogresscb_updatedeletepercent"]
old-location: picacq\iphotoacquireprogresscb_updatedeletepercent.htm
tech.root: picacq
ms.assetid: 8b555d9b-1d01-43ad-b267-8d53023390e8
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],UpdateDeletePercent method, IPhotoAcquireProgressCB.UpdateDeletePercent, IPhotoAcquireProgressCB::UpdateDeletePercent, IPhotoAcquireProgressCBUpdateDeletePercent, UpdateDeletePercent, UpdateDeletePercent method [Picture Acquisition], UpdateDeletePercent method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::UpdateDeletePercent, picacq.iphotoacquireprogresscb_updatedeletepercent
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
 - IPhotoAcquireProgressCB::UpdateDeletePercent
 - photoacquire/IPhotoAcquireProgressCB::UpdateDeletePercent
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
 - IPhotoAcquireProgressCB.UpdateDeletePercent
---

# IPhotoAcquireProgressCB::UpdateDeletePercent


## -description

The <code>UpdateDeletePercent</code> method provides extended functionality when the percentage of items deleted changes. The application provides the implementation of the <code>UpdateDeletePercent</code> method.

## -parameters

### -param nPercent [in]

Integer value containing the percentage of items deleted.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>