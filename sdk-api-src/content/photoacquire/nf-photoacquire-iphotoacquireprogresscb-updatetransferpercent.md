---
UID: NF:photoacquire.IPhotoAcquireProgressCB.UpdateTransferPercent
title: IPhotoAcquireProgressCB::UpdateTransferPercent (photoacquire.h)
description: The UpdateTransferPercent method provides extended functionality when the percentage of items transferred changes. The application provides the implementation of the UpdateTransferPercent method.
helpviewer_keywords: ["IPhotoAcquireProgressCB interface [Picture Acquisition]","UpdateTransferPercent method","IPhotoAcquireProgressCB.UpdateTransferPercent","IPhotoAcquireProgressCB::UpdateTransferPercent","IPhotoAcquireProgressCBUpdateTransferPercent","UpdateTransferPercent","UpdateTransferPercent method [Picture Acquisition]","UpdateTransferPercent method [Picture Acquisition]","IPhotoAcquireProgressCB interface","photoacquire/IPhotoAcquireProgressCB::UpdateTransferPercent","picacq.iphotoacquireprogresscb_updatetransferpercent"]
old-location: picacq\iphotoacquireprogresscb_updatetransferpercent.htm
tech.root: picacq
ms.assetid: a868663d-f926-4b29-9e1f-7df4ec36687b
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],UpdateTransferPercent method, IPhotoAcquireProgressCB.UpdateTransferPercent, IPhotoAcquireProgressCB::UpdateTransferPercent, IPhotoAcquireProgressCBUpdateTransferPercent, UpdateTransferPercent, UpdateTransferPercent method [Picture Acquisition], UpdateTransferPercent method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::UpdateTransferPercent, picacq.iphotoacquireprogresscb_updatetransferpercent
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
 - IPhotoAcquireProgressCB::UpdateTransferPercent
 - photoacquire/IPhotoAcquireProgressCB::UpdateTransferPercent
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
 - IPhotoAcquireProgressCB.UpdateTransferPercent
---

# IPhotoAcquireProgressCB::UpdateTransferPercent


## -description

The <code>UpdateTransferPercent</code> method provides extended functionality when the percentage of items transferred changes. The application provides the implementation of the <code>UpdateTransferPercent</code> method.

## -parameters

### -param fOverall [in]

Flag that, when set to <b>TRUE</b>, indicates that the value contained in <i>nPercent</i> is a percentage of the overall transfer progress, rather than a percentage of an individual item's progress.

### -param nPercent [in]

Integer value containing the percentage of items transferred.

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