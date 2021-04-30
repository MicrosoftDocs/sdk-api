---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartTransfer
title: IPhotoAcquireProgressCB::StartTransfer (photoacquire.h)
description: The StartTransfer method provides additional processing when transfer of items from the device begins. The application provides the implementation of the StartTransfer method.
helpviewer_keywords: ["IPhotoAcquireProgressCB interface [Picture Acquisition]","StartTransfer method","IPhotoAcquireProgressCB.StartTransfer","IPhotoAcquireProgressCB::StartTransfer","IPhotoAcquireProgressCBStartTransfer","StartTransfer","StartTransfer method [Picture Acquisition]","StartTransfer method [Picture Acquisition]","IPhotoAcquireProgressCB interface","photoacquire/IPhotoAcquireProgressCB::StartTransfer","picacq.iphotoacquireprogresscb_starttransfer"]
old-location: picacq\iphotoacquireprogresscb_starttransfer.htm
tech.root: picacq
ms.assetid: 8fff67d0-5d0a-4d8d-bc59-55cb65b77147
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartTransfer method, IPhotoAcquireProgressCB.StartTransfer, IPhotoAcquireProgressCB::StartTransfer, IPhotoAcquireProgressCBStartTransfer, StartTransfer, StartTransfer method [Picture Acquisition], StartTransfer method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartTransfer, picacq.iphotoacquireprogresscb_starttransfer
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
 - IPhotoAcquireProgressCB::StartTransfer
 - photoacquire/IPhotoAcquireProgressCB::StartTransfer
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
 - IPhotoAcquireProgressCB.StartTransfer
---

# IPhotoAcquireProgressCB::StartTransfer


## -description

The <code>StartTransfer</code> method provides additional processing when transfer of items from the device begins. The application provides the implementation of the <code>StartTransfer</code> method.

## -parameters

### -param pPhotoAcquireSource [in]

Pointer to the IPhotoAcquireSource from which items are being retrieved.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any Failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
The method is not implemented.

</td>
</tr>
</table>

## -remarks

Returning an error HRESULT other than E_NOTIMPL will cause acquisition to be aborted.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>