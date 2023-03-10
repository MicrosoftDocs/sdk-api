---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartItemDelete
title: IPhotoAcquireProgressCB::StartItemDelete (photoacquire.h)
description: The StartItemDelete method provides extended functionality each time the deletion of an individual item from the device begins. The application provides the implementation of the StartItemDelete method.
helpviewer_keywords: ["IPhotoAcquireProgressCB interface [Picture Acquisition]","StartItemDelete method","IPhotoAcquireProgressCB.StartItemDelete","IPhotoAcquireProgressCB::StartItemDelete","IPhotoAcquireProgressCBStartItemDelete","StartItemDelete","StartItemDelete method [Picture Acquisition]","StartItemDelete method [Picture Acquisition]","IPhotoAcquireProgressCB interface","photoacquire/IPhotoAcquireProgressCB::StartItemDelete","picacq.iphotoacquireprogresscb_startitemdelete"]
old-location: picacq\iphotoacquireprogresscb_startitemdelete.htm
tech.root: picacq
ms.assetid: 0f4ab29d-ea9c-410d-94ab-4c4d8ed76b4d
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartItemDelete method, IPhotoAcquireProgressCB.StartItemDelete, IPhotoAcquireProgressCB::StartItemDelete, IPhotoAcquireProgressCBStartItemDelete, StartItemDelete, StartItemDelete method [Picture Acquisition], StartItemDelete method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartItemDelete, picacq.iphotoacquireprogresscb_startitemdelete
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
 - IPhotoAcquireProgressCB::StartItemDelete
 - photoacquire/IPhotoAcquireProgressCB::StartItemDelete
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
 - IPhotoAcquireProgressCB.StartItemDelete
---

# IPhotoAcquireProgressCB::StartItemDelete


## -description

The <code>StartItemDelete</code> method provides extended functionality each time the deletion of an individual item from the device begins. The application provides the implementation of the <code>StartItemDelete</code> method.

## -parameters

### -param nItemIndex [in]

Integer value containing the item index in the list of items to delete.

### -param pPhotoAcquireItem [in]

Pointer to the <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object that is being deleted.

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