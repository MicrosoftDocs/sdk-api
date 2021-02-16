---
UID: NF:photoacquire.IPhotoAcquireProgressCB.Cancelled
title: IPhotoAcquireProgressCB::Cancelled (photoacquire.h)
description: The Cancelled method provides extended functionality when a cancellation occurs during an acquisition session. The application provides the implementation of the Cancelled method.
helpviewer_keywords: ["Cancelled","Cancelled method [Picture Acquisition]","Cancelled method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","Cancelled method","IPhotoAcquireProgressCB.Cancelled","IPhotoAcquireProgressCB::Cancelled","IPhotoAcquireProgressCBCancelled","photoacquire/IPhotoAcquireProgressCB::Cancelled","picacq.iphotoacquireprogresscb_cancelled"]
old-location: picacq\iphotoacquireprogresscb_cancelled.htm
tech.root: picacq
ms.assetid: 7a37934c-dc0b-433e-99cf-6c26341e582c
ms.date: 12/05/2018
ms.keywords: Cancelled, Cancelled method [Picture Acquisition], Cancelled method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],Cancelled method, IPhotoAcquireProgressCB.Cancelled, IPhotoAcquireProgressCB::Cancelled, IPhotoAcquireProgressCBCancelled, photoacquire/IPhotoAcquireProgressCB::Cancelled, picacq.iphotoacquireprogresscb_cancelled
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
 - IPhotoAcquireProgressCB::Cancelled
 - photoacquire/IPhotoAcquireProgressCB::Cancelled
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
 - IPhotoAcquireProgressCB.Cancelled
---

# IPhotoAcquireProgressCB::Cancelled


## -description

The <code>Cancelled</code> method provides extended functionality when a cancellation occurs during an acquisition session. The application provides the implementation of the <code>Cancelled</code> method.

## -parameters

### -param pfCancelled [out]

Pointer to a flag that, when set to <b>TRUE</b>, indicates that the operation was canceled.

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
The method is not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>