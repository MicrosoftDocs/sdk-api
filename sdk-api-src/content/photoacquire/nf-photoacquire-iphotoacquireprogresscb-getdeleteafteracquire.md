---
UID: NF:photoacquire.IPhotoAcquireProgressCB.GetDeleteAfterAcquire
title: IPhotoAcquireProgressCB::GetDeleteAfterAcquire (photoacquire.h)
description: The GetDeleteAfterAcquire method returns a value indicating whether photos should be deleted after acquisition.
helpviewer_keywords: ["GetDeleteAfterAcquire","GetDeleteAfterAcquire method [Picture Acquisition]","GetDeleteAfterAcquire method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","GetDeleteAfterAcquire method","IPhotoAcquireProgressCB.GetDeleteAfterAcquire","IPhotoAcquireProgressCB::GetDeleteAfterAcquire","IPhotoAcquireProgressCBGetDeleteAfterAcquire","photoacquire/IPhotoAcquireProgressCB::GetDeleteAfterAcquire","picacq.iphotoacquireprogresscb_getdeleteafteracquire"]
old-location: picacq\iphotoacquireprogresscb_getdeleteafteracquire.htm
tech.root: picacq
ms.assetid: a9e3fb54-e152-4fbd-b745-852719aabeec
ms.date: 12/05/2018
ms.keywords: GetDeleteAfterAcquire, GetDeleteAfterAcquire method [Picture Acquisition], GetDeleteAfterAcquire method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],GetDeleteAfterAcquire method, IPhotoAcquireProgressCB.GetDeleteAfterAcquire, IPhotoAcquireProgressCB::GetDeleteAfterAcquire, IPhotoAcquireProgressCBGetDeleteAfterAcquire, photoacquire/IPhotoAcquireProgressCB::GetDeleteAfterAcquire, picacq.iphotoacquireprogresscb_getdeleteafteracquire
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
 - IPhotoAcquireProgressCB::GetDeleteAfterAcquire
 - photoacquire/IPhotoAcquireProgressCB::GetDeleteAfterAcquire
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
 - IPhotoAcquireProgressCB.GetDeleteAfterAcquire
---

# IPhotoAcquireProgressCB::GetDeleteAfterAcquire


## -description

The <code>GetDeleteAfterAcquire</code> method returns a value indicating whether photos should be deleted after acquisition.

## -parameters

### -param pfDeleteAfterAcquire [out]

Pointer to a flag that, when set to <b>TRUE</b>, indicates that photos should be deleted after acquisition.

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