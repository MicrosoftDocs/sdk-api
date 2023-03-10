---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartDelete
title: IPhotoAcquireProgressCB::StartDelete (photoacquire.h)
description: The StartDelete method provides extended functionality when deletion of items from the device begins.
helpviewer_keywords: ["IPhotoAcquireProgressCB interface [Picture Acquisition]","StartDelete method","IPhotoAcquireProgressCB.StartDelete","IPhotoAcquireProgressCB::StartDelete","IPhotoAcquireProgressCBStartDelete","StartDelete","StartDelete method [Picture Acquisition]","StartDelete method [Picture Acquisition]","IPhotoAcquireProgressCB interface","photoacquire/IPhotoAcquireProgressCB::StartDelete","picacq.iphotoacquireprogresscb_startdelete"]
old-location: picacq\iphotoacquireprogresscb_startdelete.htm
tech.root: picacq
ms.assetid: 510999eb-068e-41e9-98b7-de6e67dbfe2f
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartDelete method, IPhotoAcquireProgressCB.StartDelete, IPhotoAcquireProgressCB::StartDelete, IPhotoAcquireProgressCBStartDelete, StartDelete, StartDelete method [Picture Acquisition], StartDelete method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartDelete, picacq.iphotoacquireprogresscb_startdelete
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
 - IPhotoAcquireProgressCB::StartDelete
 - photoacquire/IPhotoAcquireProgressCB::StartDelete
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
 - IPhotoAcquireProgressCB.StartDelete
---

# IPhotoAcquireProgressCB::StartDelete


## -description

The <code>StartDelete</code> method provides extended functionality when deletion of items from the device begins.



The implementation of <code>StartDelete</code> is provided by the application.

## -parameters

### -param pPhotoAcquireSource [in]

Pointer to the <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource</a> that items are being deleted from.

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
The method is not yet implemented

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>